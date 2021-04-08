---
title: Сообщение TCM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент из элемента управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- Элементы управления Windows для TCM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989229"
---
# <a name="tcm_deleteitem-message"></a><span data-ttu-id="af469-105">\_Сообщение DELETEITEM TCM</span><span class="sxs-lookup"><span data-stu-id="af469-105">TCM\_DELETEITEM message</span></span>

<span data-ttu-id="af469-106">Удаляет элемент из элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="af469-106">Removes an item from a tab control.</span></span> <span data-ttu-id="af469-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="af469-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af469-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af469-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af469-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af469-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af469-110">Индекс удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="af469-110">Index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="af469-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af469-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af469-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="af469-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af469-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af469-113">Return value</span></span>

<span data-ttu-id="af469-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="af469-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="af469-115">Требования</span><span class="sxs-lookup"><span data-stu-id="af469-115">Requirements</span></span>



| <span data-ttu-id="af469-116">Требование</span><span class="sxs-lookup"><span data-stu-id="af469-116">Requirement</span></span> | <span data-ttu-id="af469-117">Значение</span><span class="sxs-lookup"><span data-stu-id="af469-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af469-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af469-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af469-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af469-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af469-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af469-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af469-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af469-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af469-122">Header</span><span class="sxs-lookup"><span data-stu-id="af469-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af469-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="af469-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





