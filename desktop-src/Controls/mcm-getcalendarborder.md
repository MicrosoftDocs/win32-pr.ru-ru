---
title: Сообщение MCM_GETCALENDARBORDER (Коммктрл. h)
description: Возвращает размер границы в пикселях. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткуррентвиев.
ms.assetid: 68366ee1-7511-46a5-aab0-a42fb80c265f
keywords:
- Элементы управления Windows для MCM_GETCALENDARBORDER сообщений
topic_type:
- apiref
api_name:
- MCM_GETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581eeb5c060f725d3f884f4c19d7d3da3023c63a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534679"
---
# <a name="mcm_getcalendarborder-message"></a><span data-ttu-id="a81cb-105">\_Сообщение MCM жеткалендарбордер</span><span class="sxs-lookup"><span data-stu-id="a81cb-105">MCM\_GETCALENDARBORDER message</span></span>

<span data-ttu-id="a81cb-106">Возвращает размер границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a81cb-106">Gets the size of the border, in pixels.</span></span> <span data-ttu-id="a81cb-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жеткуррентвиев**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="a81cb-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a81cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a81cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a81cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a81cb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a81cb-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a81cb-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a81cb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a81cb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a81cb-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a81cb-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a81cb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a81cb-113">Return value</span></span>

<span data-ttu-id="a81cb-114">Размер границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a81cb-114">Border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="a81cb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a81cb-115">Requirements</span></span>



| <span data-ttu-id="a81cb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a81cb-116">Requirement</span></span> | <span data-ttu-id="a81cb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a81cb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a81cb-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a81cb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a81cb-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a81cb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a81cb-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a81cb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a81cb-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a81cb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a81cb-122">Header</span><span class="sxs-lookup"><span data-stu-id="a81cb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a81cb-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a81cb-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





