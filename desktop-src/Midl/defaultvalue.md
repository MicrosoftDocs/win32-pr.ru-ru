---
title: defaultvalue - атрибут
description: Атрибут \ DefaultValue \ позволяет указать значение по умолчанию для типизированного необязательного параметра.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- атрибут DefaultValue MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337268"
---
# <a name="defaultvalue-attribute"></a>defaultvalue - атрибут

Атрибут **\[ DefaultValue \]** позволяет указать значение по умолчанию для типизированного необязательного параметра.

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя интерфейса.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции, к которой будет применен атрибут **\[ DefaultValue \]** .

</dd> <dt>

*обязательный параметр-param-List* 
</dt> <dd>

Указывает обязательные параметры.

</dd> <dt>

*Список атрибутов* 
</dt> <dd>

Задает список из одного или нескольких атрибутов, разделенных запятыми, которые применяются к параметру.

</dd> <dt>

*Param-Type* 
</dt> <dd>

Указывает тип необязательного параметра.

</dd> <dt>

*Param-Name* 
</dt> <dd>

Указывает имя необязательного параметра.

</dd> <dt>

*Необязательный параметр-param-List* 
</dt> <dd>

Указывает ноль или более дополнительных параметров, каждое из которых должно иметь значение по умолчанию.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Значение по умолчанию, заданное для параметра, может быть любой константой или выражением, которое разрешается в константу, которое может быть представлено **вариантом**. В частности, атрибут **\[ \] DefaultValue** нельзя применять к параметру, который является структурой, массивом или типом **SAFEARRAY** .

Компилятор MIDL принимает следующий порядок параметров (слева направо):

1.  Обязательные параметры (параметры, у которых нет **\[ DefaultValue \]** или **\[** [**необязательных**](optional.md) **\]** атрибутов);
2.  необязательные параметры с атрибутом **\[ DefaultValue \]** или без него
3.  параметры с **\[ необязательным \]** атрибутом и без атрибута **\[ DefaultValue \]** ,
4.  **\[** параметр [**LCID**](lcid.md) **\]** , если он есть,
5.  **\[**[**retval**](retval.md) **\]** параметр

## <a name="examples"></a>Примеры

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**намного**](lcid.md)
</dt> <dt>

[**используемых**](optional.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 