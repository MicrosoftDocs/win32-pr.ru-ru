---
title: usesgetlasterror - атрибут
description: Атрибут \ усесжетластеррор \ сообщает вызывающему объекту, что он может вызвать GetLastError для получения кода ошибки.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- атрибут усесжетластеррор MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239486792eb218d51c305f9955331e90c6c165586153dab167f2e19d3a0324e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641039"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror - атрибут

Атрибут **\[ усесжетластеррор \]** сигнализирует вызывающему объекту, что он может вызвать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для получения кода ошибки.

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибуты модуля* 
</dt> <dd>

Ноль или несколько атрибутов MIDL, которые будут применены к [**модулю**](module.md).

</dd> <dt>

*имя модуля* 
</dt> <dd>

Имя идентификатора [**модуля**](module.md).

</dd> <dt>

*Идентификатор записи* 
</dt> <dd>

Указывает точку входа модуля — имя функции или целочисленный идентификационный номер.

</dd> <dt>

*другие атрибуты* 
</dt> <dd>

Ноль или несколько атрибутов MIDL, которые будут применены к удаленной процедуре.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Тип данных, возвращаемых удаленной процедурой после завершения.

</dd> <dt>

*имя функции* 
</dt> <dd>

Имя удаленной процедуры, как определено в IDL-файле.

</dd> <dt>

*Param-List* 
</dt> <dd>

Ноль или более параметров для удаленной процедуры.

</dd> </dl>

## <a name="remarks"></a>Remarks

атрибут **\[ усесжетластеррор \]** можно задать в точке входа модуля, если эта точка входа использует функцию Windows [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) для возврата кодов ошибок. Атрибут сообщает вызывающему объекту, что при возникновении ошибки при вызове этой функции вызывающий объект может вызвать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для получения кода ошибки.

## <a name="examples"></a>Примеры

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 