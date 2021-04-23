---
title: Сообщение HDM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент из элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса DeleteItem.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- Элементы управления Windows для HDM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071781"
---
# <a name="hdm_deleteitem-message"></a><span data-ttu-id="54d2f-105">\_Сообщение DELETEITEM HDM</span><span class="sxs-lookup"><span data-stu-id="54d2f-105">HDM\_DELETEITEM message</span></span>

<span data-ttu-id="54d2f-106">Удаляет элемент из элемента управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="54d2f-106">Deletes an item from a header control.</span></span> <span data-ttu-id="54d2f-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="54d2f-107">You can send this message explicitly or use the [**Header\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="54d2f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="54d2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d2f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54d2f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54d2f-110">Индекс удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="54d2f-110">An index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="54d2f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54d2f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="54d2f-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="54d2f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d2f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54d2f-113">Return value</span></span>

<span data-ttu-id="54d2f-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="54d2f-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d2f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="54d2f-115">Requirements</span></span>



| <span data-ttu-id="54d2f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="54d2f-116">Requirement</span></span> | <span data-ttu-id="54d2f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="54d2f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54d2f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54d2f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="54d2f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54d2f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54d2f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54d2f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="54d2f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54d2f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54d2f-122">Header</span><span class="sxs-lookup"><span data-stu-id="54d2f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="54d2f-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="54d2f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





