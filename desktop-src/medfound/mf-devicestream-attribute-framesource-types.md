---
description: Представляет тип источника кадра.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Атрибут MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692665"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a><span data-ttu-id="2e745-103">\_ \_ \_ \_ Атрибут фрамесаурце Types для атрибута MF девицестреам</span><span class="sxs-lookup"><span data-stu-id="2e745-103">MF\_DEVICESTREAM\_ATTRIBUTE\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="2e745-104">Представляет тип источника кадра.</span><span class="sxs-lookup"><span data-stu-id="2e745-104">Represents the frame source type.</span></span>

## <a name="data-type"></a><span data-ttu-id="2e745-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2e745-105">Data type</span></span>

<span data-ttu-id="2e745-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2e745-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2e745-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e745-107">Remarks</span></span>

<span data-ttu-id="2e745-108">Это значение этого атрибута должно быть битовой маской одного или нескольких значений из перечисления [**мффрамесаурцетипес**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) .</span><span class="sxs-lookup"><span data-stu-id="2e745-108">This value of this attribute should be a bitmask of one or more values from the [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) enumeration.</span></span> <span data-ttu-id="2e745-109">Для поддержки обратной совместимости, если этот атрибут не определен для типа мультимедиа, предполагается, что оно имеет значение **мффрамесаурцетипес:: Color**.</span><span class="sxs-lookup"><span data-stu-id="2e745-109">To support backward compatibility, when this attribute is not defined for a media type, it is assumed to have the value **MFFrameSourceTypes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e745-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2e745-110">Requirements</span></span>



| <span data-ttu-id="2e745-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2e745-111">Requirement</span></span> | <span data-ttu-id="2e745-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2e745-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e745-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e745-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2e745-114">\[Только для настольных приложений Windows 10 версии 1607\]</span><span class="sxs-lookup"><span data-stu-id="2e745-114">Windows 10, version 1607 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2e745-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e745-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2e745-116">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2e745-116">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2e745-117">Header</span><span class="sxs-lookup"><span data-stu-id="2e745-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e745-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e745-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




