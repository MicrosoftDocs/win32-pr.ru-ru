---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType=&\#0034;Number&\#0034;> , если.'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9db77cc68dab7038a1b5b9c50d49f5381ee948
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883657"
---
# <a name="numberformat"></a>numberFormat

Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType="Number"> , если. Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [NumberFormat]() .

При наличии нескольких элементов используется последний из них. Если элемент [NumberFormat]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

## <a name="syntax"></a>Синтаксис


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                   | Дочерние элементы |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Нет           |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>форматас</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; General &quot; . Задает формат вывода. Допустимы следующие значения. 
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
<td>По умолчанию. Отображает значение в виде неформатированного числа.</td>
</tr>
<tr class="even">
<td>Процент</td>
<td>Форматирует значение в процентах. Требует, чтобы свойство было UInt32.</td>
</tr>
<tr class="odd">
<td>битесизе</td>
<td>При необходимости форматирует значение как байт, &quot; КБ &quot; , &quot; МБ &quot; или &quot; ГБ &quot; . Свойство должно иметь значение UInt64.</td>
</tr>
<tr class="even">
<td>кбсизе</td>
<td>Форматирует значение в &quot; КБ &quot; , независимо от значения. Свойство должно иметь значение UInt64.</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>Форматирует значение как число битов. Требует, чтобы свойство было UInt32.</td>
</tr>
<tr class="even">
<td>Скорость</td>
<td>Форматирует значение в &quot; кбит/с &quot; . Требует, чтобы свойство было UInt32. Значение должно храниться в единицах с количеством &quot; бит в секунду &quot; .</td>
</tr>
<tr class="odd">
<td>SampleRate</td>
<td>Форматирует значение в &quot; кГц &quot; . Требует, чтобы свойство было UInt32. Значение должно храниться в &quot; &quot; единицах Герц.</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Форматирует значение в кадрах/сек. Требует, чтобы свойство было UInt32. Значение должно храниться в &quot; единицах килобайтах-Frame-to-Second &quot; .</td>
</tr>
<tr class="odd">
<td>Перекрытых</td>
<td>Форматирует значение в пикселных единицах. Требует, чтобы свойство было UInt32.</td>
</tr>
<tr class="even">
<td>DPI</td>
<td>Форматирует значение в точках на дюйм. Требует, чтобы свойство было UInt32.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Форматирует значение как длительность. Используйте &lt; форматдуратионас &gt; для указания формата длительности. Свойство должно иметь значение UInt64.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>форматдуратионас</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; чч: мм: СС &quot; . Применяется только в том случае, если <em>форматас = &quot; Duration &quot; </em>. Свойство должно иметь значение UInt64. Допустимы следующие значения. 
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>чч:мм</td>
<td>Форматирует значение в часах и минутах.</td>
</tr>
<tr class="even">
<td>чч:мм:сс</td>
<td>По умолчанию. Форматирует значение в часах, минутах и секундах.</td>
</tr>
<tr class="odd">
<td>чч: мм: СС. FFF</td>
<td>Форматирует значение в часах, минутах, секундах и миллисекундах.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
