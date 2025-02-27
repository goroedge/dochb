---
title: "Bootstrap"
date: 2024-11-12T18:49:14+03:00
draft: false
description: "Все о модуле Bootstrap, установка и его возможности"
noindex: false
featured: false
pinned: false
# comments: false
series: 
  - hugo
#  - 
categories:
  - docs
tags:
  - framework
images:
  - bs.jpg
# menu:
#   main:
#     weight: 100
#     params:
#       icon:
#         vendor: bs
#         name: book
#         color: '#e24d0e'
---

## Установка модуля
https://bootstrap.hugomods.com/tags/bootstrap/
https://bootstrap.hugomods.com/docs/
Объявления

``` yaml
markup:
  goldmark:
    renderer:
      unsafe: true
```

Установка

``` yaml
module:
  imports:
  - path: github.com/hugomods/bootstrap
```

## Alert

Алерты доступны значения
`primary, secondary, success, danger, warning, info, light and dark.`

Дальше в примерах буду писать без < и >. Т.к с ними выполняется код. Но в природе нужно ставить две скобки {{ и <, а когда закрываем, то соответственно > и еще }}.
{{% bs/collapse "Alerts code" primary true %}}
``` go-html-template
{{ bs/alert primary }}
A simple primary alert—check it out!
{{ /bs/alert }}
```
{{% /bs/collapse %}}


{{< bs/alert primary >}}
A simple primary alert—check it out!
{{< /bs/alert >}}

{{< bs/alert secondary >}}
A simple secondary alert—check it out!
{{< /bs/alert >}}

{{< bs/alert success >}}
A simple success alert—check it out!
{{< /bs/alert >}}

{{< bs/alert danger >}}
A simple danger alert—check it out!
{{< /bs/alert >}}

{{< bs/alert warning >}}
A simple warning alert—check it out!
{{< /bs/alert >}}

{{< bs/alert info >}}
A simple info alert—check it out!
{{< /bs/alert >}}

{{< bs/alert light >}}
A simple light alert—check it out!
{{< /bs/alert >}}

{{< bs/alert dark >}}
A simple dark alert—check it out!
{{< /bs/alert >}}

Или так

``` go-html-template
{{ bs/alert style=primary }}
A simple *primary alert* with Markdown—**check it out**!
{{ /bs/alert }}
```

{{% bs/alert style=primary %}}
A simple *primary alert* with Markdown—**check it out**!
{{% /bs/alert %}}

### Ссылки в Алерте
`\{\{< bs/alert-link "an example link" "#alert-link" >}}`

{{< bs/alert >}}
A simple primary alert with {{< bs/alert-link "an example link" "#alert-link" >}}. Give it a click if you like.
{{< /bs/alert >}}

### Заголовок в Алерте

{{< bs/alert success >}}
{{< bs/alert-heading "Well done!" >}}
Aww yeah, you successfully read this important alert message. This example text is going to run a bit longer so that you can see how spacing within an alert works with this kind of content.
{{< /bs/alert >}}

``` markdown
{\{< bs/alert success >}}
{\{< bs/alert-heading "Well done!" >}}
Aww yeah, you successfully read this important alert message. This example text is going to run a bit longer so that you can see how spacing within an alert works with this kind of content.
{\{< /bs/alert >}}
```

## Ссылки

{{< bs/btn-link >}}
TEXT
{{< /bs/btn-link >}}

``` markdown
{\{< bs/btn-link >}}
TEXT
{\{< /bs/btn-link >}}
```

или в одну строку `{\{< bs/btn-link text=TEXT />}}` {{< bs/btn-link text=TEXT />}}

У них тоже могут быть стили и ссылки: style options:
`primary, secondary, success, danger, warning, info, light, dark, link`

{{< bs/btn-link "#button-link-styles" "primary" >}}
Primary
{{< /bs/btn-link >}}

{{< bs/btn-link url="#button-link-styles" style="secondary" text="Secondary" />}}

{{< bs/btn-link "#button-link-styles" "success" >}}
Success
{{< /bs/btn-link >}}

{{< bs/btn-link "#button-link-styles" "danger" >}}
Danger
{{< /bs/btn-link >}}

{{< bs/btn-link "#button-link-styles" "warning" >}}
Warning
{{< /bs/btn-link >}}

{{< bs/btn-link "#button-link-styles" "info" >}}
Info
{{< /bs/btn-link >}}

{{< bs/btn-link "#button-link-styles" "light" >}}
Light
{{< /bs/btn-link >}}

{{< bs/btn-link "#button-link-styles" "dark" >}}
Dark
{{< /bs/btn-link >}}

{{< bs/btn-link  "#button-link-styles" "link" >}}
Link
{{< /bs/btn-link >}}

``` markdown
{{&lt bs/btn-link "#button-link-styles" "primary" >}}
Primary
{{&lt /bs/btn-link >}}

{{&lt bs/btn-link url="#button-link-styles" style="secondary" text="Secondary" />}}

{{&lt bs/btn-link "#button-link-styles" "success" >}}
Success
{{&lt /bs/btn-link >}}

{{&lt bs/btn-link "#button-link-styles" "danger" >}}
Danger
{{&lt /bs/btn-link >}}

{{&lt bs/btn-link "#button-link-styles" "warning" >}}
Warning
{{&lt /bs/btn-link >}}

{{&lt bs/btn-link "#button-link-styles" "info" >}}
Info
{{&lt /bs/btn-link >}}

{{&lt bs/btn-link "#button-link-styles" "light" >}}
Light
{{&lt /bs/btn-link >}}

{{&lt bs/btn-link "#button-link-styles" "dark" >}}
Dark
{{&lt /bs/btn-link >}}

{{&lt bs/btn-link  "#button-link-styles" "link" >}}
Link
{{&lt /bs/btn-link >}}
markdown


```

## Clearfix

Приклеивает контент влево и вправо
{{% bs/clearfix %}}
FLOATING CONTENT.
{{% /bs/clearfix %}}
Сразу после текста 
{{% bootstrap/clearfix %}} FLOATING CONTENT. {{% /bs/clearfix %}}

## collapse

Схлопывающийся текст

{{< bs/collapse heading="1. Step One" expand=true >}}
First of all ...
{{< /bs/collapse >}}

{{% bs/collapse "2. Step Two" secondary %}}
And then ...
{{% /bs/collapse %}}

{{% bs/collapse "3. Step Three" success %}}
**Well done**.
{{% /bs/collapse %}}

``` markdown
{\{< bs/collapse heading="1. Step One" expand=true >}}
First of all ...
{\{< /bs/collapse >}}

{\{% bs/collapse "2. Step Two" secondary %}}
And then ...
{\{% /bs/collapse %}}

{\{% bs/collapse "3. Step Three" success %}}
**Well done**.
{\{% /bs/collapse %}}
```

{{< bs/collapse heading="Configuration" expand=true >}}
  {{< bs/config-toggle hugo >}}
  params:
    message: "Hello world!"
  {{< /bs/config-toggle >}}
{{< /bs/collapse >}}

{{% bs/collapse "Template" %}}
  ```go-html-template
  <div class="greeting">
    {{ site.Params.message }}
  </div>
  ```
{{% /bs/collapse %}}

## config-tuggle

{{< bootstrap/config-toggle title="Front Matter" delimiter=true >}}
title: Hello World!
{{< /bootstrap/config-toggle >}}

## Display

{{% bs/display %}}
Display 1
{{% /bs/display %}}

``` markdown
{\{% bs/display %}}
Display 1
{\{% /bs/display %}}
```
от 1 до 6 уровня, плюс цвета

{{% bs/display level=6 class="text-success" %}}
Display 6 with extra classes via named parameters.
{{% /bs/display %}}

``` markdown
{\{% bs/display level=6 class="text-success" %}}
Display 6 with extra classes via named parameters.
{\{% /bs/display %}}
```

## Lead

выделить текст
{{% bs/lead class="text-primary" %}}
This is another lead paragraph with extra classes.
{{% /bs/lead %}}

``` markdown
{\{% bs/lead class="text-primary" %}}
This is another lead paragraph with extra classes.
{\{% /bs/lead %}}
```

## Ratio

{{< bs/ratio 1x1 >}}
  {{< bilibili BV1iT411B7yH >}}
{{< /bs/ratio >}}

Aspect Ratio 4x3
{{< bs/ratio 4x3 >}}
  {{< bilibili BV1iT411B7yH >}}
{{< /bs/ratio >}}

Aspect Ratio 16x9
{{< bs/ratio 16x9 >}}
  {{< bilibili BV1iT411B7yH >}}
{{< /bs/ratio >}}

``` text
{\{< bs/ratio 16x9 >}}
  {\{< bilibili BV1iT411B7yH >}}
{\{< /bs/ratio >}}
```

## Toggle Shortcode

{{< bs/toggle foobar >}}

  {{% bs/toggle-item Foo %}}
    *Foo* Content with **Markdown**
  
  {{% /bs/toggle-item %}}

  {{< bs/toggle-item Bar >}}
  Bar Content without Markdown
  {{< /bs/toggle-item >}}

{{< /bs/toggle >}}


  {\{< bs/toggle foobar >}}

  {\{% bs/toggle-item Foo %}}
  
  *Foo* Content with **Markdown**
  
  {\{% /bs/toggle-item %}}

  {\{< bs/toggle-item Bar >}}
  
  Bar Content without Markdown
  
  {\{< /bs/toggle-item >}}

{\{< /bs/toggle >}}


## Accordion
{\{< bs/accordion "accordion.faq" >}}
{\{< bs/accordion data="accordion.faq" flush=true alwaysOpen=true >}}

## Article Cards

{\{< bs/article-cards limit=3 >}}

## Icon

{{< bs/icon-grid data="features" border=false >}}
https://bootstrap.hugomods.com/tags/bootstrap/
