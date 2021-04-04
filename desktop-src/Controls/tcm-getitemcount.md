---
title: Сообщение TCM_GETITEMCOUNT (Коммктрл. h)
description: Извлекает число вкладок в наборе вкладок. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- Элементы управления Windows для TCM_GETITEMCOUNT сообщений
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137274"
---
# <a name="tcm_getitemcount-message"></a><span data-ttu-id="70c79-105">\_Сообщение GETITEMCOUNT TCM</span><span class="sxs-lookup"><span data-stu-id="70c79-105">TCM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="70c79-106">Извлекает число вкладок в наборе вкладок.</span><span class="sxs-lookup"><span data-stu-id="70c79-106">Retrieves the number of tabs in the tab control.</span></span> <span data-ttu-id="70c79-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="70c79-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="70c79-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="70c79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70c79-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70c79-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="70c79-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="70c79-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="70c79-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70c79-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="70c79-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="70c79-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70c79-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70c79-113">Return value</span></span>

<span data-ttu-id="70c79-114">Возвращает количество элементов в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="70c79-114">Returns the number of items if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c79-115">Требования</span><span class="sxs-lookup"><span data-stu-id="70c79-115">Requirements</span></span>



| <span data-ttu-id="70c79-116">Требование</span><span class="sxs-lookup"><span data-stu-id="70c79-116">Requirement</span></span> | <span data-ttu-id="70c79-117">Значение</span><span class="sxs-lookup"><span data-stu-id="70c79-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70c79-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70c79-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70c79-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70c79-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70c79-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70c79-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70c79-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70c79-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70c79-122">Header</span><span class="sxs-lookup"><span data-stu-id="70c79-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c79-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c79-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





