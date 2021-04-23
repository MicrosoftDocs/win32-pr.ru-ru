---
title: Перечисление WMDRMNET_POLICY_TYPE (Вмдрмсдк. h)
description: '\_ \_ Тип перечисления тип политики вмдрмнет перечисляет типы политик, доступных для операций с сетевыми устройствами Windows Media DRM.'
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Формат Windows Media WMDRMNET_POLICY_TYPE перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648902"
---
# <a name="wmdrmnet_policy_type-enumeration"></a><span data-ttu-id="796d0-105">\_ \_ Перечисление типов политики вмдрмнет</span><span class="sxs-lookup"><span data-stu-id="796d0-105">WMDRMNET\_POLICY\_TYPE enumeration</span></span>

<span data-ttu-id="796d0-106">Тип **перечисления \_ \_ тип политики вмдрмнет** перечисляет типы политик, доступных для операций с сетевыми устройствами Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="796d0-106">The **WMDRMNET\_POLICY\_TYPE** enumeration type lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="796d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="796d0-107">Syntax</span></span>


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a><span data-ttu-id="796d0-108">Константы</span><span class="sxs-lookup"><span data-stu-id="796d0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="796d0-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_тип политики вмдрмнет не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="796d0-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET\_POLICY\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="796d0-110">Неопределенные типы политик не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="796d0-110">Undefined policy types are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="796d0-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_тип политики \_ вмдрмнет \_ транскриптплай**</span><span class="sxs-lookup"><span data-stu-id="796d0-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**</span></span>
</dt> <dd>

<span data-ttu-id="796d0-112">Политика управляет возможностью преобразования содержимого, защищенного Windows Media DRM, в защищенный Windows Media DRM для данных сетевых устройств и их воспроизведения на сетевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="796d0-112">The policy governs the ability to convert content protected by Windows Media DRM into protected Windows Media DRM for Network Devices data and play it back on a networked device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="796d0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="796d0-113">Remarks</span></span>

<span data-ttu-id="796d0-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="796d0-114">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="796d0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="796d0-115">Requirements</span></span>



| <span data-ttu-id="796d0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="796d0-116">Requirement</span></span> | <span data-ttu-id="796d0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="796d0-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="796d0-118">Header</span><span class="sxs-lookup"><span data-stu-id="796d0-118">Header</span></span><br/> | <dl> <span data-ttu-id="796d0-119"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="796d0-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="796d0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="796d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="796d0-121">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="796d0-121">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="796d0-122">**\_Политика вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="796d0-122">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





