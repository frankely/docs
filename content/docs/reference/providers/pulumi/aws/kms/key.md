---
title: "Key"
---

<!-- WARNING: this file was generated by the Pulumi Terraform Bridge (tfgen) Tool. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

<style>
  table td p { margin-top: 0; margin-bottom: 0; }
</style>

Provides a KMS customer master key.

> This content is derived from https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/kms_key.html.markdown.


## Create a Key Resource

{{< langchoose csharp >}}

<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new</span> <span class="nx"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#Key>Key</a></span><span class="p">(</span><span class="nx">name</span>: <span class="kt"><a href=https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String>string</a></span><span class="p">,</span> <span class="nx">args?</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#KeyArgs>KeyArgs</a></span><span class="p">,</span> <span class="nx">opts?</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions>pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>

```python
def __init__(__self__, resource_name, opts=None, customer_master_key_spec=None, deletion_window_in_days=None, description=None, enable_key_rotation=None, is_enabled=None, key_usage=None, policy=None, tags=None, __props__=None)
```

```go
func NewKey(ctx *pulumi.Context, name string, args *KeyArgs, opts ...pulumi.ResourceOption) (*Key, error)

```

```csharp
public Key(string name, KeyArgs? args = null, CustomResourceOptions? options = null)

```

Creates a Key resource with the given unique name, arguments, and options.

{{% lang nodejs %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Optional) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang go %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Optional) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang csharp %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Optional) The arguments to use to populate this resource's properties.</li>
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
            <td class="align-top">customer<wbr>Master<wbr>Key<wbr>Spec</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether the key contains a symmetric key or an asymmetric key pair and the encryption algorithms or signing algorithms that the key supports.
Valid values: `SYMMETRIC_DEFAULT`,  `RSA_2048`, `RSA_3072`, `RSA_4096`, `ECC_NIST_P256`, `ECC_NIST_P384`, `ECC_NIST_P521`, or `ECC_SECG_P256K1`. Defaults to `SYMMETRIC_DEFAULT`. For help with choosing a key spec, see the [AWS KMS Developer Guide](https://docs.aws.amazon.com/kms/latest/developerguide/symm-asymm-choose.html).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">deletion<wbr>Window<wbr>In<wbr>Days</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
(Optional) Duration in days after which the key is deleted
after destruction of the resource, must be between 7 and 30 days. Defaults to 30 days.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">description</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The description of the key as viewed in AWS console.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enable<wbr>Key<wbr>Rotation</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether [key rotation](http://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html)
is enabled. Defaults to false.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">is<wbr>Enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether the key is enabled. Defaults to true.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">key<wbr>Usage</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies the intended use of the key. Valid values: `ENCRYPT_DECRYPT` or `SIGN_VERIFY`.
Defaults to `ENCRYPT_DECRYPT`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">policy</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">tags</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) A mapping of tags to assign to the object.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Key Output Properties

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
            <td class="align-top">arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The Amazon Resource Name (ARN) of the key.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">customer<wbr>Master<wbr>Key<wbr>Spec</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
Specifies whether the key contains a symmetric key or an asymmetric key pair and the encryption algorithms or signing algorithms that the key supports.
Valid values: `SYMMETRIC_DEFAULT`,  `RSA_2048`, `RSA_3072`, `RSA_4096`, `ECC_NIST_P256`, `ECC_NIST_P384`, `ECC_NIST_P521`, or `ECC_SECG_P256K1`. Defaults to `SYMMETRIC_DEFAULT`. For help with choosing a key spec, see the [AWS KMS Developer Guide](https://docs.aws.amazon.com/kms/latest/developerguide/symm-asymm-choose.html).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">deletion<wbr>Window<wbr>In<wbr>Days</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
Duration in days after which the key is deleted
after destruction of the resource, must be between 7 and 30 days. Defaults to 30 days.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">description</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The description of the key as viewed in AWS console.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enable<wbr>Key<wbr>Rotation</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
Specifies whether [key rotation](http://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html)
is enabled. Defaults to false.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">is<wbr>Enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
Specifies whether the key is enabled. Defaults to true.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">key<wbr>Id</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The globally unique identifier for the key.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">key<wbr>Usage</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
Specifies the intended use of the key. Valid values: `ENCRYPT_DECRYPT` or `SIGN_VERIFY`.
Defaults to `ENCRYPT_DECRYPT`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">policy</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">tags</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
A mapping of tags to assign to the object.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Look up an Existing Key Resource

{{< langchoose csharp >}}

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: KeyState, opts?: pulumi.CustomResourceOptions): Key;
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

Get an existing Key resource's state with the given name, ID, and optional extra
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
            <td class="align-top">arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The Amazon Resource Name (ARN) of the key.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">customer<wbr>Master<wbr>Key<wbr>Spec</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether the key contains a symmetric key or an asymmetric key pair and the encryption algorithms or signing algorithms that the key supports.
Valid values: `SYMMETRIC_DEFAULT`,  `RSA_2048`, `RSA_3072`, `RSA_4096`, `ECC_NIST_P256`, `ECC_NIST_P384`, `ECC_NIST_P521`, or `ECC_SECG_P256K1`. Defaults to `SYMMETRIC_DEFAULT`. For help with choosing a key spec, see the [AWS KMS Developer Guide](https://docs.aws.amazon.com/kms/latest/developerguide/symm-asymm-choose.html).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">deletion<wbr>Window<wbr>In<wbr>Days</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
(Optional) Duration in days after which the key is deleted
after destruction of the resource, must be between 7 and 30 days. Defaults to 30 days.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">description</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The description of the key as viewed in AWS console.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enable<wbr>Key<wbr>Rotation</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether [key rotation](http://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html)
is enabled. Defaults to false.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">is<wbr>Enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether the key is enabled. Defaults to true.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">key<wbr>Id</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The globally unique identifier for the key.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">key<wbr>Usage</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies the intended use of the key. Valid values: `ENCRYPT_DECRYPT` or `SIGN_VERIFY`.
Defaults to `ENCRYPT_DECRYPT`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">policy</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">tags</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) A mapping of tags to assign to the object.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Import an Existing Key Resource

TODO

## Support Types
