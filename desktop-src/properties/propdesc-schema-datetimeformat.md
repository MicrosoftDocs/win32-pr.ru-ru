---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType=&\#0034;DateTime&\#0034;> , если.'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950f10106d7850f4a5b58aeb165e8cb4cc9ffcd4
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629176"
---
# <a name="datetimeformat"></a>dateTimeFormat

Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType="DateTime"> , если. Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [DateTimeFormat]() .

При наличии нескольких элементов используется последний из них. Если элемент [DateTimeFormat]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

## <a name="syntax"></a>Синтаксис


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                   | Дочерние элементы |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | None           |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>форматас</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; General &quot; . Допустимы следующие значения. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Общие сведения</td>
<td>По умолчанию. Форматирует значение даты и времени с помощью <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>шформатдатетиме</strong></a>. Используйте атрибуты <em>форматтимеас</em> и <em>форматдатеас</em> для указания способа форматирования даты и времени. Требует, чтобы тип свойства был типом DateTime.</td>
</tr>
<tr class="even">
<td>Месяц</td>
<td>Форматирует значение как один из месяцев года. Требует, чтобы тип свойства был Int32. Значение должно храниться как числовое значение, равное 1, представляющему первый месяц года.</td>
</tr>
<tr class="odd">
<td>еармонс</td>
<td>Форматирует значение как &quot; год-месяц &quot; . Требует, чтобы тип свойства был Int32. Значение должно храниться таким, что два старших байта указывают год, а младшие два байта указывают месяц.</td>
</tr>
<tr class="even">
<td>Year;</td>
<td>Форматирует значение как простую строку.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>форматтимеас</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; шорттиме &quot; . Задает формат для вывода времени. Применяется, если <strong>форматас &quot; = &quot; General</strong>. Допустимы следующие значения. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>шорттиме</td>
<td>По умолчанию. Показывать время, например &quot; 7:48 PM &quot; .</td>
</tr>
<tr class="even">
<td>Давнего</td>
<td>Показывать время, например &quot; 7:48:33 PM &quot; .</td>
</tr>
<tr class="odd">
<td>хидетиме</td>
<td>Не отображать временную часть даты.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>форматдатеас</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; шортдате &quot; . Задает формат для вывода даты. Применяется, если <strong>форматас &quot; = &quot; General</strong>. Допустимы следующие значения. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Пример</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>шортдате</td>
<td>По умолчанию. Отображение даты, например &quot; 5/13/59 &quot; .</td>
</tr>
<tr class="even">
<td>лонгдате</td>
<td>Отображение даты, например &quot; среды, 13 мая 1959 &quot; .</td>
</tr>
<tr class="odd">
<td>хидедате</td>
<td>Не отображать дату.</td>
</tr>
<tr class="even">
<td>релативешортдате</td>
<td>Показывать дату, такую как &quot; шортдате &quot; , но при возможности использовать относительные описания, например, &quot; вчера &quot; .</td>
</tr>
<tr class="odd">
<td>релативелонгдате</td>
<td>Показывать дату, такую как &quot; лонгдате &quot; , но при возможности использовать относительные описания, например, &quot; вчера &quot; .</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
