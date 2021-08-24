---
title: Ресурс МЕНУЕКС
description: Определяет содержимое ресурса меню. | Ресурс МЕНУЕКС
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Меню ресурсов МЕНУЕКС и другие ресурсы
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec78bd0d33b48b11de77fe7742affb4265160752ffad30d72ecf3e9c173bb77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825944"
---
# <a name="menuex-resource"></a>Ресурс МЕНУЕКС

Определяет содержимое ресурса меню. Ресурс меню — это коллекция сведений, определяющих внешний вид и функции меню приложения. Меню — это специальное средство ввода, которое позволяет пользователю выбирать команды и открывать подменю из списка пунктов меню. Он также определяет следующее:

-   Идентификаторы справки в меню.
-   Идентификаторы в меню.
-   Использование флагов **MFT \_ \** _ типа и флагов состояния _*MFA \_ \**_ . Дополнительные сведения об этих флагах см. в описании структуры [_ *объектами menuiteminfo* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)
</dt> <dd>

Определяет пункт меню.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*итемтекст*
</dt> <dd>

Строка, содержащая текст для пункта меню. Дополнительные сведения см. в разделе [**MenuItem**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*удостоверения*
</dt> <dd>

Числовое выражение, указывающее идентификатор элемента меню.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Тип*
</dt> <dd>

Числовое выражение, указывающее тип элемента меню для использования предопределенных \_ \* значений типа MFT, включите следующую инструкцию в RC-файл:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*с*
</dt> <dd>

Числовое выражение, указывающее состояние пункта меню для использования предопределенных \_ \* значений состояния MFA, включите следующую инструкцию в. RC-файл:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**ПОДСКАЗКИ**](popup-resource.md)
</dt> <dd>

Определяет пункт меню с связанным подменю.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*итемтекст*
</dt> <dd>

Строка, содержащая текст для пункта меню.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*удостоверения*
</dt> <dd>

Числовое выражение, указывающее идентификатор элемента меню.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Тип*
</dt> <dd>

Числовое выражение, указывающее тип элемента меню для использования предопределенных \_ \* значений типа MFT, включите следующую инструкцию в. RC-файл:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*с*
</dt> <dd>

Числовое выражение, указывающее состояние пункта меню для использования предопределенных \_ \* значений состояния MFA, включите следующую инструкцию в RC-файл:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*Идентификатор справки*
</dt> <dd>

Числовое выражение, указывающее идентификатор, используемый для идентификации меню во время обработки [**\_ справки WM**](../shell/wm-help.md) .

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*попупбоди*
</dt> <dd>

Содержит любое сочетание инструкций [**MenuItem**](menuitem-statement.md) и [**Popup**](popup-resource.md) .

</dd> </dl>

Для обратной совместимости также поддерживаются некоторые атрибуты. Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).

## <a name="remarks"></a>Remarks

Допустимые арифметические и логические операции, которые могут содержаться в любом из числовых выражений в инструкциях **менуекс** , приведены ниже.

-   Добавить ("+")
-   Вычитание ("-")
-   Унарный минус ("-")
-   Унарный оператор NOT (' ~ ')
-   И (' & ')
-   ИЛИ (' \| ')

## <a name="see-also"></a>См. также

<dl> <dt>

[Использование меню](./using-menus.md)
</dt> <dt>

[**Accelerator**](accelerators-resource.md)
</dt> <dt>

[**ПОКАЗАТЕЛИ**](characteristics-statement.md)
</dt> <dt>

[**Откроется**](dialog-resource.md)
</dt> <dt>

[**ЯЗЫКЕ**](language-statement.md)
</dt> <dt>

[**МЕНЮ**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**ПОДСКАЗКИ**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**ВЕРСИЯ**](version-statement.md)
</dt> </dl>

 

 
