---
title: Сообщение LVM_GETORIGIN (Коммктрл. h)
description: Возвращает начало текущего представления для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса «источник ListView».
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Элементы управления Windows для LVM_GETORIGIN сообщений
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137110"
---
# <a name="lvm_getorigin-message"></a><span data-ttu-id="821c4-105">Сообщение LVM о \_ происхождении</span><span class="sxs-lookup"><span data-stu-id="821c4-105">LVM\_GETORIGIN message</span></span>

<span data-ttu-id="821c4-106">Возвращает начало текущего представления для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="821c4-106">Retrieves the current view origin for a list-view control.</span></span> <span data-ttu-id="821c4-107">Это сообщение можно отправить явно или с помощью макроса [**« \_ источник ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) ».</span><span class="sxs-lookup"><span data-stu-id="821c4-107">You can send this message explicitly or by using the [**ListView\_GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="821c4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="821c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="821c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="821c4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="821c4-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="821c4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="821c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="821c4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="821c4-112">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , которая получает источник представления.</span><span class="sxs-lookup"><span data-stu-id="821c4-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the view origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="821c4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="821c4-113">Return value</span></span>

<span data-ttu-id="821c4-114">Возвращает **значение true** в случае успешного выполнения или **false** , если текущее представление является списком или представлением отчетов.</span><span class="sxs-lookup"><span data-stu-id="821c4-114">Returns **TRUE** if successful, or **FALSE** if the current view is list or report view.</span></span>

## <a name="requirements"></a><span data-ttu-id="821c4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="821c4-115">Requirements</span></span>



| <span data-ttu-id="821c4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="821c4-116">Requirement</span></span> | <span data-ttu-id="821c4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="821c4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="821c4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="821c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="821c4-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="821c4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="821c4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="821c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="821c4-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="821c4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="821c4-122">Header</span><span class="sxs-lookup"><span data-stu-id="821c4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="821c4-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="821c4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

