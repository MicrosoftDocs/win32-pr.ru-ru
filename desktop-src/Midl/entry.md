---
title: entry - атрибут
description: Атрибут \ Entry \ указывает экспортированную функцию или константу в модуле, определяя точку входа в библиотеке DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- элемент атрибута MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f6dab1681cb04adbd48c4a27c14a359c87624870a43c118c6dd1a589689c00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013932"
---
# <a name="entry-attribute"></a>entry - атрибут

Атрибут **\[ entry \]** указывает экспортированную функцию или константу в модуле, определяя точку входа в библиотеке DLL.

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для [**модуля**](module.md).

</dd> <dt>

*Идентификатор записи* 
</dt> <dd>

Указывает имя функции точки входа модуля или целочисленный идентификационный номер.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Указывает ноль или более атрибутов для применения компилятора MIDL к [**модулю**](module.md).

</dd> <dt>

*ModuleName* 
</dt> <dd>

Указывает имя, используемое другими компонентами программного обеспечения для обозначения [**модуля**](module.md).

</dd> <dt>

*елементлист* 
</dt> <dd>

Указывает одну или несколько инструкций определения элемента модуля.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если переменная *EntryID* атрибута **\[ entry \]** является строкой, это именованная точка входа. Если идентификатор *EntryID* является числом, точка входа определяется порядковым номером. Этот атрибут предоставляет способ получения адреса функции в модуле.

## <a name="examples"></a>Примеры

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a>См. также

<dl> <dt>

[**dllname**](dllname-str-.md)
</dt> <dt>

[**модуль**](module.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 