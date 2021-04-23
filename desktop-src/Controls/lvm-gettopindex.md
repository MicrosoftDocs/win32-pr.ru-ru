---
title: Сообщение LVM_GETTOPINDEX (Коммктрл. h)
description: Получает индекс самого верхнего видимого элемента в списке или представлении отчетов. Это сообщение можно отправить явно или с помощью \_ макроса Жеттопиндекс ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Элементы управления Windows для LVM_GETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654649"
---
# <a name="lvm_gettopindex-message"></a><span data-ttu-id="62630-105">\_Сообщение LVM жеттопиндекс</span><span class="sxs-lookup"><span data-stu-id="62630-105">LVM\_GETTOPINDEX message</span></span>

<span data-ttu-id="62630-106">Получает индекс самого верхнего видимого элемента в списке или представлении отчетов.</span><span class="sxs-lookup"><span data-stu-id="62630-106">Retrieves the index of the topmost visible item when in list or report view.</span></span> <span data-ttu-id="62630-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жеттопиндекс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .</span><span class="sxs-lookup"><span data-stu-id="62630-107">You can send this message explicitly or by using the [**ListView\_GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="62630-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="62630-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62630-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62630-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62630-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="62630-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="62630-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62630-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="62630-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="62630-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62630-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62630-113">Return value</span></span>

<span data-ttu-id="62630-114">Возвращает индекс элемента, если он был успешным.</span><span class="sxs-lookup"><span data-stu-id="62630-114">Returns the index of the item if successful.</span></span> <span data-ttu-id="62630-115">Возвращает нуль, если элемент управления "представление списка" находится в виде значка или маленького значка или если элемент управления "представление списка" находится в представлении Details с включенными группами.</span><span class="sxs-lookup"><span data-stu-id="62630-115">Returns zero if the list-view control is in icon or small icon view, or if the list-view control is in details view with groups enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="62630-116">Требования</span><span class="sxs-lookup"><span data-stu-id="62630-116">Requirements</span></span>



| <span data-ttu-id="62630-117">Требование</span><span class="sxs-lookup"><span data-stu-id="62630-117">Requirement</span></span> | <span data-ttu-id="62630-118">Значение</span><span class="sxs-lookup"><span data-stu-id="62630-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62630-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62630-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62630-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62630-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62630-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62630-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62630-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62630-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62630-123">Header</span><span class="sxs-lookup"><span data-stu-id="62630-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62630-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="62630-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





