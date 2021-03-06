---

copyright:

  years: 2018

lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 为访问组创建动态规则
{: #rules}

您可以创建动态规则，以根据特定身份属性自动将联合用户添加到访问组。当用户使用联合标识登录时，身份提供者中的数据会根据设置的规则，将用户动态映射到访问组。
{:shortdesc}

用户已经在您公司的域中拥有特定的身份信息，并且他们使用联合标识登录时，可以使用 SAML 断言来传递此数据。在身份提供者内配置的 SAML 断言或属性语句提供了用于创建每个规则的数据。例如，可能有将用户定义为管理员的 true 或 false 属性语句。此信息可用于将作为管理员的所有用户添加到 {{site.data.keyword.Bluemix_notm}} 帐户中已创建的特定管理员访问组。有关更多信息，请参阅[示例规则](accessgroup_rules.html#example)。

只有已受邀加入帐户的用户才能使用动态规则映射到访问组。
{: note}

## 设置规则

动态规则通过设置条件而创建，这些条件必须与身份提供者内所配置并在登录期间使用用户联合标识传入的数据相匹配。要创建规则，请执行以下步骤：

1. 在菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后选择**访问组**。
2. 选择要为其创建规则的访问组的名称，以打开“组详细信息”页面。
3. 选择**动态规则**选项卡。
4. 单击**添加规则**。
5. 输入身份提供者的信息。以下列表提供了各个必填字段的详细信息。

<dl>
<dt>名称</dt>
<dd>输入规则的定制名称，以帮助您记住要添加到访问组的用户类型。</dd>
<dt>身份提供者</dt>
<dd>输入身份提供者的 URI。这是身份提供者的 SAML“entityId”字段，有时也称为签发者标识，作为联合配置的一部分用于通过 IBM 标识上线。</dd>
<dt>到期时间（小时）</dt>
<dd>可以使用此选项通过为分配的访问权设置时间限制，提供额外的安全性。每个用户必须每 24 小时登录一次来刷新其访问权，但您可以将访问权设置为最短一小时到期。在此时间段到期后，将撤销组成员资格。</dd>
<dt>满足以下条件时添加用户</dt>
<dd>必须在此字段中输入属性语句名称。此值特定于身份提供者。</dd>
<dt>比较符</dt>
<dd>可以选择“等于”、“不等于”、“等于（忽略大小写）”、“不等于（忽略大小写）”、In 或“包含”。属性语句具有数组类型时，请使用“包含”选项。此外，您还可以使用 In 选项输入多个要匹配的值。</dd>
<dt>值</dt>
<dd>输入规则要与之比较的属性语句的属性值。</dd>
</dl>

可以为一个规则添加多个条件。必须满足规则中设置的所有条件才能将用户添加到访问组。
{: tip}

## 示例规则
{: #example}

以下示例包含**添加规则**页面上每个字段的值。在此规则中，在联合身份提供者内识别为管理员的用户将映射到仅为管理员设置特定访问权的 {{site.data.keyword.Bluemix_notm}} 访问组。

|字段|值|
|----------|---------|
|名称|管理员组规则|
|身份提供者|`https://idp.example.org/SAML2`|
|到期时间（小时）|12|
|满足以下条件时添加用户（属性名称）|isManager|
|比较符|等于|
|值|true|
{: caption="表 1. 访问组的示例动态规则" caption-side="top"}
