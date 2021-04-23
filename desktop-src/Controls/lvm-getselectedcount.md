---
title: Сообщение LVM_GETSELECTEDCOUNT (Коммктрл. h)
description: Определяет число выбранных элементов в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жетселектедкаунт ListView.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- Элементы управления Windows для LVM_GETSELECTEDCOUNT сообщений
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892445"
---
# <a name="lvm_getselectedcount-message"></a><span data-ttu-id="80f02-105">\_Сообщение LVM жетселектедкаунт</span><span class="sxs-lookup"><span data-stu-id="80f02-105">LVM\_GETSELECTEDCOUNT message</span></span>

<span data-ttu-id="80f02-106">Определяет число выбранных элементов в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="80f02-106">Determines the number of selected items in a list-view control.</span></span> <span data-ttu-id="80f02-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетселектедкаунт ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) .</span><span class="sxs-lookup"><span data-stu-id="80f02-107">You can send this message explicitly or by using the [**ListView\_GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="80f02-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="80f02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80f02-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80f02-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="80f02-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="80f02-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="80f02-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80f02-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="80f02-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="80f02-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80f02-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80f02-113">Return value</span></span>

<span data-ttu-id="80f02-114">Возвращает число выбранных элементов.</span><span class="sxs-lookup"><span data-stu-id="80f02-114">Returns the number of selected items.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f02-115">Требования</span><span class="sxs-lookup"><span data-stu-id="80f02-115">Requirements</span></span>



| <span data-ttu-id="80f02-116">Требование</span><span class="sxs-lookup"><span data-stu-id="80f02-116">Requirement</span></span> | <span data-ttu-id="80f02-117">Значение</span><span class="sxs-lookup"><span data-stu-id="80f02-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80f02-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80f02-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80f02-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80f02-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80f02-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80f02-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80f02-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="80f02-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80f02-122">Header</span><span class="sxs-lookup"><span data-stu-id="80f02-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80f02-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="80f02-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





