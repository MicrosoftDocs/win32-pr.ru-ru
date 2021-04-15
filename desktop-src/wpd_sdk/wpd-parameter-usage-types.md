---
description: '\_ \_ \_ Тип перечисления типы использования параметра WPD описывает, как параметр метода используется в данном методе.'
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Перечисление WPD_PARAMETER_USAGE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648129"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>\_ \_ Перечисление типов использования параметров WPD \_

Тип [**перечисления \_ \_ \_ типы использования параметра WPD**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) описывает, как параметр метода используется в данном методе.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_ \_ возвращаемое использование параметра WPD \_**
</dt> <dd>

Параметр получает возвращаемое значение, если оно указано в методе.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_Использование параметра \_ WPD \_ в**
</dt> <dd>

Параметр содержит входное значение до вызова метода.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_Использование параметра \_ WPD \_**
</dt> <dd>

Параметр содержит выходное значение при возврате из метода.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_Использование параметра \_ WPD \_ InOut**
</dt> <dd>

Параметр содержит входное значение до вызова метода и выходное значение при его возврате.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



 

