---
title: Сообщение TCM_DELETEALLITEMS (Коммктрл. h)
description: Удаляет все элементы из элемента управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл делетеаллитемс.
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- Элементы управления Windows для TCM_DELETEALLITEMS сообщений
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73a91cd6ec3b5472b6e7da2127f8224062cfbbc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535123"
---
# <a name="tcm_deleteallitems-message"></a><span data-ttu-id="d3130-105">\_Сообщение ДЕЛЕТЕАЛЛИТЕМС TCM</span><span class="sxs-lookup"><span data-stu-id="d3130-105">TCM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="d3130-106">Удаляет все элементы из элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="d3130-106">Removes all items from a tab control.</span></span> <span data-ttu-id="d3130-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ делетеаллитемс**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="d3130-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3130-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3130-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3130-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3130-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d3130-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d3130-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d3130-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3130-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d3130-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d3130-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3130-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3130-113">Return value</span></span>

<span data-ttu-id="d3130-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d3130-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3130-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d3130-115">Requirements</span></span>



| <span data-ttu-id="d3130-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d3130-116">Requirement</span></span> | <span data-ttu-id="d3130-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d3130-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3130-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3130-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d3130-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3130-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3130-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3130-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d3130-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3130-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3130-122">Header</span><span class="sxs-lookup"><span data-stu-id="d3130-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3130-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3130-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





