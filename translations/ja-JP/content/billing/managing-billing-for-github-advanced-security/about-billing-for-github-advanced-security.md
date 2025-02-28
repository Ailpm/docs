---
title: About billing for GitHub Advanced Security
intro: 'If you want to use {% data variables.product.prodname_GH_advanced_security %} features{% ifversion fpt or ghec %} in a private or internal repository{% endif %}, you need a license{% ifversion fpt %} for your enterprise{% endif %}.{% ifversion fpt or ghec %} These features are available free of charge for public repositories on {% data variables.product.prodname_dotcom_the_website %}.{% endif %}'
product: '{% data reusables.gated-features.ghas %}'
redirect_from:
  - /admin/advanced-security/about-licensing-for-github-advanced-security
  - /billing/managing-licensing-for-github-advanced-security/about-licensing-for-github-advanced-security
  - /github/setting-up-and-managing-billing-and-payments-on-github/about-licensing-for-github-advanced-security
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-licensing-for-github-advanced-security/about-licensing-for-github-advanced-security
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
type: overview
topics:
  - Advanced Security
  - Enterprise
  - Licensing
shortTitle: Advanced Security billing
---

## {% data variables.product.prodname_GH_advanced_security %}の支払いについて

{% ifversion fpt %}

If you want to use {% data variables.product.prodname_GH_advanced_security %} features on any repository apart from a public repository on {% data variables.product.prodname_dotcom_the_website %}, you will need a {% data variables.product.prodname_GH_advanced_security %} license, available with {% data variables.product.prodname_ghe_cloud %} or {% data variables.product.prodname_ghe_server %}. {% data variables.product.prodname_GH_advanced_security %} に関する詳しい情報については、「[{% data variables.product.prodname_GH_advanced_security %} について](/github/getting-started-with-github/about-github-advanced-security)」を参照してください。

{% elsif ghec %}

If you want to use {% data variables.product.prodname_GH_advanced_security %} features on any repository apart from a public repository on {% data variables.product.prodname_dotcom_the_website %}, you will need a {% data variables.product.prodname_GH_advanced_security %} license. {% data variables.product.prodname_GH_advanced_security %} に関する詳しい情報については、「[{% data variables.product.prodname_GH_advanced_security %} について](/github/getting-started-with-github/about-github-advanced-security)」を参照してください。

{% elsif ghes %}

You can make extra features for code security available to users by buying and uploading a license for {% data variables.product.prodname_GH_advanced_security %}. {% data variables.product.prodname_GH_advanced_security %} に関する詳しい情報については、「[{% data variables.product.prodname_GH_advanced_security %} について](/github/getting-started-with-github/about-github-advanced-security)」を参照してください。

{% endif %}

{% ifversion fpt or ghes or ghec %}

{% data reusables.advanced-security.license-overview %}

{% endif %}

To discuss licensing {% data variables.product.prodname_GH_advanced_security %} for your enterprise, contact {% data variables.contact.contact_enterprise_sales %}.

## {% data variables.product.prodname_GH_advanced_security %} のコミッター番号について

{% data reusables.advanced-security.about-committer-numbers-ghec-ghes %}

{% ifversion fpt or ghes or ghec %}

{% data reusables.advanced-security.managing-license-usage-ghec-ghes %}

{% endif %}

Enterprise アカウントが所有する Organization による {% data variables.product.prodname_advanced_security %} の使用を許可または禁止するポリシーを適用できます。 For more information, see "[Enforcing policies for {% data variables.product.prodname_advanced_security %} in your enterprise]({% ifversion fpt %}/enterprise-cloud@latest/{% endif %}/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-advanced-security-in-your-enterprise){% ifversion fpt %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}."{% endif %}

{% ifversion fpt or ghes or ghec %}

ライセンスの使用状況の表示について詳しくは、「[{% data variables.product.prodname_GH_advanced_security %} の使用状況を表示する](/billing/managing-billing-for-github-advanced-security/viewing-your-github-advanced-security-usage)」を参照してください。

{% endif %}

## Understanding active committer usage

The following example timeline demonstrates how active committer count for {% data variables.product.prodname_GH_advanced_security %} could change over time in an enterprise. For each month, you will find events, along with the resulting committer count.

<table spaces-before="0">
  <tr>
    <th align="left">
      日付
    </th>
    
    <th align="left">
      Events during the month
    </th>
    
    <th align="right">
      Total committers
    </th>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>15 年 4 月</nobr>
    </td>
    
    <td align="left">
      A member of your enterprise enables {% data variables.product.prodname_GH_advanced_security %} for repository <strong x-id="1">X</strong>. Repository <strong x-id="1">X</strong> has 50 committers over the past 90 days.
    </td>
    
    <td align="right">
      <strong x-id="1">50</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>May 1</nobr>
    </td>
    
    <td align="left">
      Developer <strong x-id="1">A</strong> leaves the team working on repository <strong x-id="1">X</strong>. Developer <strong x-id="1">A</strong>'s contributions continue to count for 90 days.
    </td>
    
    <td align="right">
      <strong x-id="1">50</strong> | <strong x-id="1">50</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>August 1</nobr>
    </td>
    
    <td align="left">
      Developer <strong x-id="1">A</strong>'s contributions no longer count towards the licences required, because 90 days have passed.
    </td>
    
    <td align="right">
      <sub>_50 - 1_</sub></br><strong x-id="1">49</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>15 年 8 月</nobr>
    </td>
    
    <td align="left">
      A member of your enterprise enables {% data variables.product.prodname_GH_advanced_security %} for a second repository, repository <strong x-id="1">Y</strong>. In the last 90 days, a total of 20 developers contributed to that repository. Of those 20 developers, 10 also recently worked on repo <strong x-id="1">X</strong> and do not require additional licenses.
    </td>
    
    <td align="right">
      <sub>_49 + 10_</sub><br/><strong x-id="1">59</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>16 年 8 月</nobr>
    </td>
    
    <td align="left">
      A member of your enterprise disables {% data variables.product.prodname_GH_advanced_security %} for repository <strong x-id="1">X</strong>. Of the 49 developers who were working on repository <strong x-id="1">X</strong>, 10 still also work on repository <strong x-id="1">Y</strong>, which has a total of 20 developers contributing in the last 90 days.
    </td>
    
    <td align="right">
      <sub>_49 - 29_</sub><br/><strong x-id="1">20</strong>
    </td>
  </tr>
</table>

{% note %}

**Note:** A user will be flagged as active when their commits are pushed to any branch of a repository, even if the commits were authored more than 90 days ago.

{% endnote %}

## Getting the most out of {% data variables.product.prodname_GH_advanced_security %}

{% data reusables.advanced-security.getting-the-most-from-your-license %}
