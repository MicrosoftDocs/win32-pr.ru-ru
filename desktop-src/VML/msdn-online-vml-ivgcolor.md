---
title: Ивгколор VML
description: Ивгколор VML
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d4800fbb99557acfbd3fd6e0dbbd893f30158f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487893"
---
# <a name="vml-ivgcolor"></a>Ивгколор VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Задает цвет.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Атрибуты</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Строка</td>
<td>Строка. Текстовое представление цвета. Поддерживаются следующие именованные типы цветов:
<ul>
<li>Черный (#000000)</li>
<li>Серебро (#C0C0C0)</li>
<li>Серый (#808080)</li>
<li>Белый (#FFFFFF)</li>
<li>Каштановый (#800000)</li>
<li>Красный (#FF0000)</li>
<li>Сиреневый (#800080)</li>
<li>Фучсиа (#FF00FF)</li>
<li>Зеленый (#008000)</li>
<li>Травяной (#00FF00)</li>
<li>Оливковый (#808000)</li>
<li>Желтый (#FFFF00)</li>
<li>ВМФ (#000080)</li>
<li>Синий (#0000FF)</li>
<li>Бирюзовый (#008080)</li>
<li>Голубой (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Тип</td>
<td>Вгколортипе. Тип цвета. Один из следующих типов:
<ul>
<li>Смешанный</li>
<li>RGB</li>
<li>Схема</li>
<li>именованная</li>
</ul></td>
</tr>
<tr class="odd">
<td>RGB</td>
<td>Вгргбтипе. Значение RGB (<strong>Long</strong>) цвета. Допустим только в том случае, если тип — &quot; <strong>RGB</strong> &quot; .</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Integer</strong>. Красный компонент цвета. Может находиться в диапазоне от 0 до 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Integer</strong>. Зеленый компонент цвета. Может находиться в диапазоне от 0 до 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Integer</strong>. Синий компонент цвета. Может находиться в диапазоне от 0 до 255.</td>
</tr>
</tbody>
</table>



 

 

 