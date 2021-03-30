---
description: Указывает тип единицы, содержащейся в Имфсампле \_ коллекции мфсампликстенсион форвардеддекодеунитс.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: Перечисление MF_CUSTOM_DECODE_UNIT_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263632"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a><span data-ttu-id="23399-103">\_ \_ \_ \_ Перечисление типов единиц для НАСТРАИВАЕМого расшифровки MF</span><span class="sxs-lookup"><span data-stu-id="23399-103">MF\_CUSTOM\_DECODE\_UNIT\_TYPE enumeration</span></span>

<span data-ttu-id="23399-104">Указывает тип единицы, содержащейся в [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) коллекции [мфсампликстенсион \_ форвардеддекодеунитс](mfsampleextension-forwardeddecodeunits.md) .</span><span class="sxs-lookup"><span data-stu-id="23399-104">Specifies the type of unit contained in an [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in a [MFSampleExtension\_ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) collection.</span></span>

## <a name="members"></a><span data-ttu-id="23399-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="23399-105">Members</span></span>



| <span data-ttu-id="23399-106">Член</span><span class="sxs-lookup"><span data-stu-id="23399-106">Member</span></span>                    | <span data-ttu-id="23399-107">Описание</span><span class="sxs-lookup"><span data-stu-id="23399-107">Description</span></span>                                                             | <span data-ttu-id="23399-108">Значение</span><span class="sxs-lookup"><span data-stu-id="23399-108">Value</span></span> |
|---------------------------|-------------------------------------------------------------------------|-------|
| <span data-ttu-id="23399-109">**MF \_ декодирование \_ единицы \_ NAL**</span><span class="sxs-lookup"><span data-stu-id="23399-109">**MF\_DECODE\_UNIT\_NAL**</span></span> | <span data-ttu-id="23399-110">Тип единицы — это единица уровня абстрагирования сети (НАЛУ).</span><span class="sxs-lookup"><span data-stu-id="23399-110">The unit type is network abstraction layer unit (NALU).</span></span> <br/>     | <span data-ttu-id="23399-111">0</span><span class="sxs-lookup"><span data-stu-id="23399-111">0</span></span>     |
| <span data-ttu-id="23399-112">**\_расшифровка \_ \_ Sei единицы**</span><span class="sxs-lookup"><span data-stu-id="23399-112">**MF\_DECODE\_UNIT\_SEI**</span></span> | <span data-ttu-id="23399-113">Тип единицы — дополнительная информация об улучшении (SEI).</span><span class="sxs-lookup"><span data-stu-id="23399-113">The unit type is Supplemental Enhancement Information (SEI).</span></span><br/> | <span data-ttu-id="23399-114">1</span><span class="sxs-lookup"><span data-stu-id="23399-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="23399-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="23399-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="23399-116">Требования</span><span class="sxs-lookup"><span data-stu-id="23399-116">Requirements</span></span>



| <span data-ttu-id="23399-117">Требование</span><span class="sxs-lookup"><span data-stu-id="23399-117">Requirement</span></span> | <span data-ttu-id="23399-118">Значение</span><span class="sxs-lookup"><span data-stu-id="23399-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23399-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23399-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23399-120">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="23399-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="23399-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23399-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23399-122">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="23399-122">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="23399-123">Header</span><span class="sxs-lookup"><span data-stu-id="23399-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23399-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="23399-124"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




