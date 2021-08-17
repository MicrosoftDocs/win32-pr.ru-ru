---
title: retval - атрибут
description: Атрибут \ retval \ обозначает параметр, который получает возвращаемое значение элемента.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- атрибут retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72655883b24c83890cf2f5604cb8f7335c6943b32e5e69611dba415689b03e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146307"
---
# <a name="retval-attribute"></a>retval - атрибут

Атрибут **\[ retval \]** задает параметр, который получает возвращаемое значение элемента.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Тип данных возвращаемого значения удаленной процедуры.

</dd> <dt>

*имя функции* 
</dt> <dd>

Имя, используемое для вызова удаленной процедуры.

</dd> <dt>

*необязательные атрибуты* 
</dt> <dd>

Ноль или несколько атрибутов MIDL.

</dd> <dt>

*тип данных* 
</dt> <dd>

Тип данных, передаваемых через параметр.

</dd> <dt>

*Param-Name* 
</dt> <dd>

Имя идентификатора параметра.

</dd> </dl>

## <a name="remarks"></a>Remarks

Атрибут **\[ retval \]** можно использовать для параметров членов интерфейса, описывающих методы или получения свойств. (Атрибут является обязательным для последнего параметра метода, имеющего **\[** [**propget**](propget.md) **\]** атрибут.) Параметр должен иметь **\[** атрибут [**out**](out-idl.md) **\]** и должен быть типом указателя.

**\[** [**Необязательный**](optional.md) **\]** атрибут нельзя применить к параметру **\[ retval \]** .

Компилятор MIDL принимает следующий порядок параметров (слева направо):

1.  Обязательные параметры (параметры, у которых нет **\[** [**DefaultValue**](defaultvalue.md) **\]** или **\[** [**необязательных**](optional.md) **\]** атрибутов).
2.  Необязательные параметры с **\[** атрибутом [**DefaultValue**](defaultvalue.md) или без него **\]** .
3.  Параметры с **\[** [**необязательным**](optional.md) **\]** атрибутом и без **\[** [](defaultvalue.md) **\]** атрибута DefaultValue.
4.  **\[** параметр [**LCID**](lcid.md) **\]** , если он есть.
5.  параметр **\[ retval \]** .

Параметры с атрибутом **\[ retval \]** не отображаются в ориентированных на пользователей браузерах.

### <a name="flags"></a>Флаги

ИДЛФЛАГ \_ фретвал

## <a name="examples"></a>Примеры

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**максимально**](defaultvalue.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**намного**](lcid.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**используемых**](optional.md)
</dt> <dt>

[**заполняет**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**типефлагс**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 