---
title: Строковый элемент
description: Представляет строковый ресурс.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- элемент строки Windows лента
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a34a417b6ad4d57bea83fcae13d810b22114271
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630960"
---
# <a name="string-element"></a>Строковый элемент

Представляет строковый ресурс.

## <a name="usage"></a>Использование

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Содержимое</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Уникальный идентификатор ресурса. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем. <br/> Максимальная длина — 10 символов, включая необязательные нули в начале. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Символ</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Символ ресурса для строки.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Буква или символ подчеркивания, за которым следует любая последовательность букв, цифр или знаков подчеркивания.<br/> Максимальная длина — 100 символов.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                   | Описание                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String. Content**](windowsribbon-element-string-content.md)<br/> | Может выполняться не более одного раза<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Может выполняться не более одного раза<br/> <br/> |
| [**String. Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Command. keytip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Command. Лабелдескриптион**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Command. Лабелтитле**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Command. Тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Command. Тултиптитле**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждой [**команды Command. лабелтитле**](windowsribbon-element-command-labeltitle.md), [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. тултиптитле**](windowsribbon-element-command-tooltiptitle.md)или элемента [**Command. тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md) .

Определение строки добавляется в файл заголовка ленты, например `#define strSave 59999` .

Строка добавляется в таблицу строк в файле ресурсов ленты, где платформа Ribbon создает имя и идентификатор, если они не объявлены.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **строки** .


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a>Сведения об элементе

- **минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: нет



 

 





