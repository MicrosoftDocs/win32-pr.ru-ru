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
# <a name="wpd_parameter_usage_types-enumeration"></a><span data-ttu-id="ba1da-103">\_ \_ Перечисление типов использования параметров WPD \_</span><span class="sxs-lookup"><span data-stu-id="ba1da-103">WPD\_PARAMETER\_USAGE\_TYPES enumeration</span></span>

<span data-ttu-id="ba1da-104">Тип [**перечисления \_ \_ \_ типы использования параметра WPD**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) описывает, как параметр метода используется в данном методе.</span><span class="sxs-lookup"><span data-stu-id="ba1da-104">The [**WPD\_PARAMETER\_USAGE\_TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) enumeration type describes how a method parameter is used in a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba1da-105">Syntax</span></span>


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="ba1da-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ba1da-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ba1da-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_ \_ возвращаемое использование параметра WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ba1da-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD\_PARAMETER\_USAGE\_RETURN**</span></span>
</dt> <dd>

<span data-ttu-id="ba1da-108">Параметр получает возвращаемое значение, если оно указано в методе.</span><span class="sxs-lookup"><span data-stu-id="ba1da-108">The parameter receives the return value, if specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="ba1da-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_Использование параметра \_ WPD \_ в**</span><span class="sxs-lookup"><span data-stu-id="ba1da-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD\_PARAMETER\_USAGE\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="ba1da-110">Параметр содержит входное значение до вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ba1da-110">The parameter contains an input value before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="ba1da-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_Использование параметра \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ba1da-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD\_PARAMETER\_USAGE\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="ba1da-112">Параметр содержит выходное значение при возврате из метода.</span><span class="sxs-lookup"><span data-stu-id="ba1da-112">The parameter contains an output value when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="ba1da-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_Использование параметра \_ WPD \_ InOut**</span><span class="sxs-lookup"><span data-stu-id="ba1da-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD\_PARAMETER\_USAGE\_INOUT**</span></span>
</dt> <dd>

<span data-ttu-id="ba1da-114">Параметр содержит входное значение до вызова метода и выходное значение при его возврате.</span><span class="sxs-lookup"><span data-stu-id="ba1da-114">The parameter contains an input value before the method is called and an output value when it returns.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba1da-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ba1da-115">Requirements</span></span>



| <span data-ttu-id="ba1da-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ba1da-116">Requirement</span></span> | <span data-ttu-id="ba1da-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ba1da-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1da-118">Header</span><span class="sxs-lookup"><span data-stu-id="ba1da-118">Header</span></span><br/> | <dl> <span data-ttu-id="ba1da-119"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba1da-119"><dt>PortableDevice.h</dt></span></span> </dl> |



 

