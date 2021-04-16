---
description: Извлекает шрифт, с которым элемент управления в данный момент рисует свой текст.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Сообщение WM_GETFONT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702574"
---
# <a name="wm_getfont-message"></a><span data-ttu-id="711d9-103">Сообщение WM. \_ Font</span><span class="sxs-lookup"><span data-stu-id="711d9-103">WM\_GETFONT message</span></span>

<span data-ttu-id="711d9-104">Извлекает шрифт, с которым элемент управления в данный момент рисует свой текст.</span><span class="sxs-lookup"><span data-stu-id="711d9-104">Retrieves the font with which the control is currently drawing its text.</span></span>


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a><span data-ttu-id="711d9-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="711d9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711d9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="711d9-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="711d9-107">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="711d9-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="711d9-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="711d9-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="711d9-109">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="711d9-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711d9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="711d9-110">Return value</span></span>

<span data-ttu-id="711d9-111">Тип: **хфонт**</span><span class="sxs-lookup"><span data-stu-id="711d9-111">Type: **HFONT**</span></span>

<span data-ttu-id="711d9-112">Возвращаемое значение является маркером шрифта, используемого элементом управления, или **значением NULL** , если элемент управления использует системный шрифт.</span><span class="sxs-lookup"><span data-stu-id="711d9-112">The return value is a handle to the font used by the control, or **NULL** if the control is using the system font.</span></span>

## <a name="requirements"></a><span data-ttu-id="711d9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="711d9-113">Requirements</span></span>



| <span data-ttu-id="711d9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="711d9-114">Requirement</span></span> | <span data-ttu-id="711d9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="711d9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="711d9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="711d9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="711d9-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="711d9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="711d9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="711d9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="711d9-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="711d9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="711d9-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="711d9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="711d9-121"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="711d9-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711d9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="711d9-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="711d9-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="711d9-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="711d9-124">**WM \_ сетфонт**</span><span class="sxs-lookup"><span data-stu-id="711d9-124">**WM\_SETFONT**</span></span>](wm-setfont.md)
</dt> <dt>

<span data-ttu-id="711d9-125">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="711d9-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="711d9-126">Windows</span><span class="sxs-lookup"><span data-stu-id="711d9-126">Windows</span></span>](windows.md)
</dt> </dl>

 

 




