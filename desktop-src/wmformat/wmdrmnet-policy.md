---
title: Структура WMDRMNET_POLICY (Вмдрмсдк. h)
description: '\_Структура политики вмдрмнет содержит политику, используемую для операций с сетевыми устройствами Windows Media DRM.'
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Формат WMDRMNET_POLICY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647959"
---
# <a name="wmdrmnet_policy-structure"></a><span data-ttu-id="10845-105">\_Структура политики вмдрмнет</span><span class="sxs-lookup"><span data-stu-id="10845-105">WMDRMNET\_POLICY structure</span></span>

<span data-ttu-id="10845-106">Структура **\_ политики вмдрмнет** содержит политику, используемую для операций с сетевыми устройствами Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="10845-106">The **WMDRMNET\_POLICY** structure contains the policy to be used for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="10845-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10845-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a><span data-ttu-id="10845-108">Члены</span><span class="sxs-lookup"><span data-stu-id="10845-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="10845-109">**еполицитипе**</span><span class="sxs-lookup"><span data-stu-id="10845-109">**ePolicyType**</span></span>
</dt> <dd>

<span data-ttu-id="10845-110">Член перечисления [**\_ \_ типа политики вмдрмнет**](wmdrmnet-policy-type.md) , указывающий тип политики.</span><span class="sxs-lookup"><span data-stu-id="10845-110">Member of the [**WMDRMNET\_POLICY\_TYPE**](wmdrmnet-policy-type.md) enumeration that specifies the type of policy.</span></span>

</dd> <dt>

<span data-ttu-id="10845-111">**пбполици**</span><span class="sxs-lookup"><span data-stu-id="10845-111">**pbPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="10845-112">Буфер, содержащий политику.</span><span class="sxs-lookup"><span data-stu-id="10845-112">Buffer containing the policy.</span></span> <span data-ttu-id="10845-113">Единственным типом политики, поддерживаемым в настоящее время, является **вмдрмнет \_ Policy \_ Type \_ транскриптплай**.</span><span class="sxs-lookup"><span data-stu-id="10845-113">The only type of policy currently supported is **WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**.</span></span> <span data-ttu-id="10845-114">Этот элемент является указателем на структуру **\_ \_ транскриптплай политики вмдрмнет** .</span><span class="sxs-lookup"><span data-stu-id="10845-114">This member is a pointer to a **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10845-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10845-115">Remarks</span></span>

<span data-ttu-id="10845-116">Эта структура используется в качестве параметра для метода [**ивмдрмнеттрансмиттер:: жетлеафлиценсереспонсе**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="10845-116">This structure is used as a parameter for the [**IWMDRMNetTransmitter::GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="10845-117">Требования</span><span class="sxs-lookup"><span data-stu-id="10845-117">Requirements</span></span>



| <span data-ttu-id="10845-118">Требование</span><span class="sxs-lookup"><span data-stu-id="10845-118">Requirement</span></span> | <span data-ttu-id="10845-119">Значение</span><span class="sxs-lookup"><span data-stu-id="10845-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10845-120">Header</span><span class="sxs-lookup"><span data-stu-id="10845-120">Header</span></span><br/> | <dl> <span data-ttu-id="10845-121"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="10845-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10845-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10845-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10845-123">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="10845-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="10845-124">**\_ \_ глобальные требования политики \_ вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="10845-124">**WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS**</span></span>](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[<span data-ttu-id="10845-125">**\_ \_ Минимальная среда политики \_ вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="10845-125">**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**</span></span>](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[<span data-ttu-id="10845-126">**\_транскриптплай политика \_ вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="10845-126">**WMDRMNET\_POLICY\_TRANSCRYPTPLAY**</span></span>](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[<span data-ttu-id="10845-127">**\_тип политики \_ вмдрмнет**</span><span class="sxs-lookup"><span data-stu-id="10845-127">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





