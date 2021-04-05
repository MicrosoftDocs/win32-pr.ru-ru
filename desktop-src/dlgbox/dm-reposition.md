---
title: Сообщение DM_REPOSITION (Winuser. h)
description: Перемещает диалоговое окно верхнего уровня таким образом, чтобы оно поместилось в область рабочего стола. Приложение может отправить это сообщение в диалоговое окно после изменения его размера, чтобы убедиться, что все диалоговое окно остается видимым.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- DM_REPOSITION диалоговых окон сообщений
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071979"
---
# <a name="dm_reposition-message"></a><span data-ttu-id="19663-105">\_Сообщение о перемещении DM</span><span class="sxs-lookup"><span data-stu-id="19663-105">DM\_REPOSITION message</span></span>

<span data-ttu-id="19663-106">Перемещает диалоговое окно верхнего уровня таким образом, чтобы оно поместилось в область рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="19663-106">Repositions a top-level dialog box so that it fits within the desktop area.</span></span> <span data-ttu-id="19663-107">Приложение может отправить это сообщение в диалоговое окно после изменения его размера, чтобы убедиться, что все диалоговое окно остается видимым.</span><span class="sxs-lookup"><span data-stu-id="19663-107">An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.</span></span>


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="19663-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="19663-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19663-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19663-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19663-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="19663-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="19663-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19663-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19663-112">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="19663-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19663-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19663-113">Return value</span></span>

<span data-ttu-id="19663-114">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="19663-114">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19663-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19663-115">Remarks</span></span>

<span data-ttu-id="19663-116">Это сообщение не действует, если диалоговое окно является дочерним окном.</span><span class="sxs-lookup"><span data-stu-id="19663-116">This message has no effect if the dialog box is a child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="19663-117">Требования</span><span class="sxs-lookup"><span data-stu-id="19663-117">Requirements</span></span>



| <span data-ttu-id="19663-118">Требование</span><span class="sxs-lookup"><span data-stu-id="19663-118">Requirement</span></span> | <span data-ttu-id="19663-119">Значение</span><span class="sxs-lookup"><span data-stu-id="19663-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19663-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19663-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19663-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19663-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="19663-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19663-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19663-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19663-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19663-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="19663-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="19663-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19663-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19663-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19663-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19663-127">Общие сведения о диалоговых окнах</span><span class="sxs-lookup"><span data-stu-id="19663-127">Dialog Boxes Overview</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





