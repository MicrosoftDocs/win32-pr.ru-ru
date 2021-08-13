---
title: vararg - атрибут
description: Атрибут \ vararg \ указывает, что функция принимает переменное число параметров. Для этого последний параметр должен быть надежным массивом типа VARIANT, который содержит все остальные параметры.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- атрибут vararg MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848393f6bad82d6793e34ba6f4da803c7dd64803c1c40e4ea05487ea141ec48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641012"
---
# <a name="vararg-attribute"></a>vararg - атрибут

Атрибут **\[ vararg \]** указывает, что функция принимает переменное число параметров. Для этого последний параметр должен быть надежным массивом типа **Variant** , который содержит все остальные параметры.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*необязательные атрибуты* 
</dt> <dd>

Указывает ноль или более атрибутов, которые должны быть применены к функции. Несколько атрибутов разделяются запятыми.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Тип данных, возвращаемых удаленной процедурой после завершения.

</dd> <dt>

*имя функции* 
</dt> <dd>

Имя удаленной процедуры.

</dd> <dt>

*Optional-param-Attributes* 
</dt> <dd>

Указывает ноль или более атрибутов, которые должны быть применены к параметру функции сразу после перечисления атрибутов.

</dd> <dt>

*Param-List* 
</dt> <dd>

Задает все параметры, сохраняет окончательный, отличающийся параметр.

</dd> <dt>

*Last-param-Name* 
</dt> <dd>

Имя изменяющегося параметра.

</dd> </dl>

## <a name="remarks"></a>Remarks

**\[** Атрибуты [**Optional**](optional.md) **\]** и DefaultValue нельзя применять **\[** [](defaultvalue.md) **\]** к параметрам в функции, имеющей атрибут **\[ vararg \]** .

## <a name="examples"></a>Примеры

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**максимально**](defaultvalue.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**используемых**](optional.md)
</dt> </dl>

 

 