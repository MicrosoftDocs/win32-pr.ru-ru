---
title: Эффект размытия DWM за константами (Двмапи. h)
description: Флаги, используемые \_ структурой БЛУРБЕХИНД DWM для указания того, какие из его членов содержат действительные сведения.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534517"
---
# <a name="dwm-blur-behind-constants"></a><span data-ttu-id="cbfab-103">Размытия в DWM за константами</span><span class="sxs-lookup"><span data-stu-id="cbfab-103">DWM Blur Behind Constants</span></span>

<span data-ttu-id="cbfab-104">Флаги, используемые структурой [**\_ блурбехинд DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) для указания того, какие из его членов содержат действительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cbfab-104">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span>

<dl> <dt>

<span data-ttu-id="cbfab-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ Enable**</span><span class="sxs-lookup"><span data-stu-id="cbfab-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM\_BB\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfab-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbfab-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="cbfab-107">Указано значение для элемента **фенабле** .</span><span class="sxs-lookup"><span data-stu-id="cbfab-107">A value for the **fEnable** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cbfab-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ блуррегион**</span><span class="sxs-lookup"><span data-stu-id="cbfab-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM\_BB\_BLURREGION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfab-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbfab-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="cbfab-110">Указано значение для элемента **хргнблур** .</span><span class="sxs-lookup"><span data-stu-id="cbfab-110">A value for the **hRgnBlur** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cbfab-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ транситиононмаксимизед**</span><span class="sxs-lookup"><span data-stu-id="cbfab-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM\_BB\_TRANSITIONONMAXIMIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbfab-112">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbfab-112">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="cbfab-113">Указано значение для элемента **фтранситиононмаксимизед** .</span><span class="sxs-lookup"><span data-stu-id="cbfab-113">A value for the **fTransitionOnMaximized** member has been specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbfab-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cbfab-114">Requirements</span></span>



| <span data-ttu-id="cbfab-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cbfab-115">Requirement</span></span> | <span data-ttu-id="cbfab-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cbfab-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfab-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbfab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cbfab-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbfab-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cbfab-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbfab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cbfab-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbfab-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cbfab-121">Header</span><span class="sxs-lookup"><span data-stu-id="cbfab-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbfab-122"><dt>Двмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbfab-122"><dt>Dwmapi.h</dt></span></span> </dl> |



 

 





