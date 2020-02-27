---
title: "PolicyAttachment"
---

<!-- WARNING: this file was generated by the Pulumi Terraform Bridge (tfgen) Tool. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

<style>
  table td p { margin-top: 0; margin-bottom: 0; }
</style>

Attaches a Managed IAM Policy to user(s), role(s), and/or group(s)

!> **WARNING:** The aws.iam.PolicyAttachment resource creates **exclusive** attachments of IAM policies. Across the entire AWS account, all of the users/roles/groups to which a single policy is attached must be declared by a single aws.iam.PolicyAttachment resource. This means that even any users/roles/groups that have the attached policy via any other mechanism (including other resources managed by this provider) will have that attached policy revoked by this resource. Consider `aws.iam.RolePolicyAttachment`, `aws.iam.UserPolicyAttachment`, or `aws.iam.GroupPolicyAttachment` instead. These resources do not enforce exclusive attachment of an IAM policy.

> **NOTE:** The usage of this resource conflicts with the `aws.iam.GroupPolicyAttachment`, `aws.iam.RolePolicyAttachment`, and `aws.iam.UserPolicyAttachment` resources and will permanently show a difference if both are defined.

> This content is derived from https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/iam_policy_attachment.html.markdown.


## Create a PolicyAttachment Resource

{{< langchoose csharp >}}

<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new</span> <span class="nx"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#PolicyAttachment>PolicyAttachment</a></span><span class="p">(</span><span class="nx">name</span>: <span class="kt"><a href=https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String>string</a></span><span class="p">,</span> <span class="nx">args</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#PolicyAttachmentArgs>PolicyAttachmentArgs</a></span><span class="p">,</span> <span class="nx">opts?</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions>pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>

```python
def __init__(__self__, resource_name, opts=None, groups=None, name=None, policy_arn=None, roles=None, users=None, __props__=None)
```

```go
func NewPolicyAttachment(ctx *pulumi.Context, name string, args *PolicyAttachmentArgs, opts ...pulumi.ResourceOption) (*PolicyAttachment, error)

```

```csharp
public PolicyAttachment(string name, PolicyAttachmentArgs args, CustomResourceOptions? options = null)

```

Creates a PolicyAttachment resource with the given unique name, arguments, and options.

{{% lang nodejs %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Required) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang go %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Required) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang csharp %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Required) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

The following arguments are supported:

<table class="ml-6">
    <thead>
        <tr>
            <th>Argument</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="align-top">groups</td>
            <td class="align-top"><code>Array&lt;<wbr>Union&lt;<wbr>string, <wbr>Group<wbr>&gt;<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) The group(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The name of the attachment. This cannot be an empty string.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">policy<wbr>Arn</td>
            <td class="align-top"><code>ARN</code></td>
            <td class="align-top">{{% md %}}
(Required) The ARN of the policy you want to apply

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">roles</td>
            <td class="align-top"><code>Array&lt;<wbr>Union&lt;<wbr>string, <wbr>Role<wbr>&gt;<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) The role(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">users</td>
            <td class="align-top"><code>Array&lt;<wbr>Union&lt;<wbr>string, <wbr>User<wbr>&gt;<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) The user(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## PolicyAttachment Output Properties

The following output properties are available:

<table class="ml-6">
    <thead>
        <tr>
            <th>Argument</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="align-top">groups</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
The group(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The name of the attachment. This cannot be an empty string.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">policy<wbr>Arn</td>
            <td class="align-top"><code>ARN</code></td>
            <td class="align-top">{{% md %}}
The ARN of the policy you want to apply

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">roles</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
The role(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">users</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
The user(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Look up an Existing PolicyAttachment Resource

{{< langchoose csharp >}}

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: PolicyAttachmentState, opts?: pulumi.CustomResourceOptions): PolicyAttachment;
```

```python
def get(resource_name, id, opts=None, acceleration_status=None, acl=None, arn=None, bucket=None, bucket_domain_name=None, bucket_prefix=None, bucket_regional_domain_name=None, cors_rules=None, force_destroy=None, hosted_zone_id=None, lifecycle_rules=None, loggings=None, object_lock_configuration=None, policy=None, region=None, replication_configuration=None, request_payer=None, server_side_encryption_configuration=None, tags=None, versioning=None, website=None, website_domain=None, website_endpoint=None)
```

```go
func GetBucket(ctx *pulumi.Context, name string, id pulumi.IDInput, state *BucketState, opts ...pulumi.ResourceOption) (*Bucket, error)
```

```csharp
public static Bucket Get(string name, Input<string> id, BucketState? state = null, CustomResourceOptions? options = null);
```

Get an existing PolicyAttachment resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% lang nodejs %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>id</strong> &ndash; (Required) The _unique_ provider ID of the resource to lookup.</li>
    <li><strong>state</strong> &ndash; (Optional) Any extra arguments used during the lookup.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang go %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>id</strong> &ndash; (Required) The _unique_ provider ID of the resource to lookup.</li>
    <li><strong>state</strong> &ndash; (Optional) Any extra arguments used during the lookup.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang csharp %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>id</strong> &ndash; (Required) The _unique_ provider ID of the resource to lookup.</li>
    <li><strong>state</strong> &ndash; (Optional) Any extra arguments used during the lookup.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

The following state arguments are supported:

<table class="ml-6">
    <thead>
        <tr>
            <th>Argument</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="align-top">groups</td>
            <td class="align-top"><code>Array&lt;<wbr>Union&lt;<wbr>string, <wbr>Group<wbr>&gt;<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) The group(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The name of the attachment. This cannot be an empty string.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">policy<wbr>Arn</td>
            <td class="align-top"><code>ARN</code></td>
            <td class="align-top">{{% md %}}
(Optional) The ARN of the policy you want to apply

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">roles</td>
            <td class="align-top"><code>Array&lt;<wbr>Union&lt;<wbr>string, <wbr>Role<wbr>&gt;<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) The role(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">users</td>
            <td class="align-top"><code>Array&lt;<wbr>Union&lt;<wbr>string, <wbr>User<wbr>&gt;<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) The user(s) the policy should be applied to

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Import an Existing PolicyAttachment Resource

TODO

## Support Types
