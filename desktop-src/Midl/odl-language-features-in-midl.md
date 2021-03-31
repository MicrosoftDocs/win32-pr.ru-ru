---
title: Функции языка ODL в MIDL
description: Атрибуты, ключевые слова, операторы и директивы языка описания объектов (ODL), которые являются частью MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL и ODL MIDL, языковые функции
- ODL MIDL, в MIDL
- ODL MIDL, атрибуты
- ODL MIDL, ключевые слова
- ODL MIDL, инструкции
- ODL MIDL, директивы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888967"
---
# <a name="odl-language-features-in-midl"></a>Функции языка ODL в MIDL

> [!Note]  
> Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL.

 

В следующих разделах перечислены атрибуты, ключевые слова, операторы и директивы языка описания объектов (ODL), которые теперь являются частью язык MIDL (MIDL):

-   [Атрибуты ODL](#odl-attributes)
-   [Ключевые слова, инструкции и директивы ODL](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a>Атрибуты ODL



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| \[[**аппобжект**](appobject.md)\]         | \[[**привязываемых**](bindable.md)\]       |
| \[[**элемента**](control.md)\]             | \[[**параметры**](default.md)\]         |
| \[[**максимально**](defaultvalue.md)\]   | \[[**дисплайбинд**](displaybind.md)\] |
| \[[**dllname**](dllname-str-.md)\]        | \[[**двойной**](dual.md)\]               |
| \[[**операции**](entry.md)\]                 | \[[**HelpContext**](helpcontext.md)\] |
| \[[**helpstring**](helpstring.md)\]       | \[[**HelpFile**](helpfile.md)\]       |
| \[[**служеб**](hidden.md)\]               | \[[**удостоверения**](id.md)\]                   |
| \[[**иммедиатебинд**](immediatebind.md)\] | \[[**окне**](in.md)\]                   |
| \[[**намного**](lcid.md)\]                   | \[[**обладателем**](licensed.md)\]       |
| \[[**nonextensible**](nonextensible.md)\] | \[[**ODL**](odl.md)\]                 |
| \[[**oleautomation**](oleautomation.md)\] | \[[**используемых**](optional.md)\]       |
| \[[**заполняет**](out-idl.md)\]                 | \[[**propget**](propget.md)\]         |
| \[[**propput**](propput.md)\]             | \[[**propputref**](propputref.md)\]   |
| \[[**закрытый**](public.md)\]               | \[[ **только для чтения**](readonly.md)\]      |
| \[[**рекуестедит**](requestedit.md)\]     | \[[**зона**](restricted.md)\]   |
| \[[**retval**](retval.md)\]               | \[[**источника**](source.md)\]           |
| \[[**UUID**](uuid.md)\]                   | [**аргумент**](vararg.md)\]             |
| \[[**Версия**](version.md)\]             | Â                                      |



 

## <a name="odl-keywords-statements-and-directives"></a>Ключевые слова, инструкции и директивы ODL



|                                        |
|----------------------------------------|
| [**кокласс**](coclass.md)             |
| [**интерфейса**](dispinterface.md) |
| [**перечисления**](enum.md)                   |
| \[[**importlib**](importlib.md)\]     |
| [**взаимодействия**](interface.md)         |
| [**библиотека**](library.md)             |
| [**модуль**](module.md)               |
| [**struct**](struct.md)               |
| [**определение**](typedef.md)             |
| [**наборов**](union.md)                 |



 

Сведения о том, как маршалировать типы OLE Automation, такие как **BSTR**, **Variant** и **SAFEARRAY**, см. в разделе [маршалирование типов данных OLE](marshaling-ole-data-types.md).

 

 




