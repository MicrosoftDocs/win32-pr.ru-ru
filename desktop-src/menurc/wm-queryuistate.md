---
title: Сообщение WM_QUERYUISTATE (Winuser. h)
description: Приложение отправляет \_ сообщение WM куерюистате для получения состояния пользовательского интерфейса для окна.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691964"
---
# <a name="wm_queryuistate-message"></a><span data-ttu-id="52ffd-104">\_Сообщение КУЕРЮИСТАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="52ffd-104">WM\_QUERYUISTATE message</span></span>

<span data-ttu-id="52ffd-105">Приложение отправляет сообщение **WM \_ куерюистате** для получения состояния пользовательского интерфейса для окна.</span><span class="sxs-lookup"><span data-stu-id="52ffd-105">An application sends the **WM\_QUERYUISTATE** message to retrieve the UI state for a window.</span></span>


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a><span data-ttu-id="52ffd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="52ffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ffd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52ffd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52ffd-108">Этот параметр не используется и должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="52ffd-108">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="52ffd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52ffd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52ffd-110">Этот параметр не используется и должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="52ffd-110">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ffd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52ffd-111">Return value</span></span>

<span data-ttu-id="52ffd-112">Возвращаемое значение равно **null** , если индикаторы фокуса и сочетания клавиш видимы.</span><span class="sxs-lookup"><span data-stu-id="52ffd-112">The return value is **NULL** if the focus indicators and the keyboard accelerators are visible.</span></span> <span data-ttu-id="52ffd-113">В противном случае возвращаемое значение может быть одним или несколькими следующими значениями.</span><span class="sxs-lookup"><span data-stu-id="52ffd-113">Otherwise, the return value can be one or more of the following values.</span></span>



| <span data-ttu-id="52ffd-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="52ffd-114">Return code/value</span></span>                                                                                                                                       | <span data-ttu-id="52ffd-115">Описание</span><span class="sxs-lookup"><span data-stu-id="52ffd-115">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52ffd-116"><dt>**Уисф \_ Активный**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="52ffd-116"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>    | <span data-ttu-id="52ffd-117">Элемент управления должен быть нарисован в стиле, используемом для активных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="52ffd-117">A control should be drawn in the style used for active controls.</span></span><br/> |
| <dl> <span data-ttu-id="52ffd-118"><dt>**Уисф \_ ХИДЕАКЦЕЛ**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="52ffd-118"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="52ffd-119">Сочетания клавиш скрыты.</span><span class="sxs-lookup"><span data-stu-id="52ffd-119">Keyboard accelerators are hidden.</span></span><br/>                                |
| <dl> <span data-ttu-id="52ffd-120"><dt>**Уисф \_ ХИДЕФОКУС**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="52ffd-120"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="52ffd-121">Индикаторы фокуса скрыты.</span><span class="sxs-lookup"><span data-stu-id="52ffd-121">Focus indicators are hidden.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="52ffd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="52ffd-122">Requirements</span></span>



| <span data-ttu-id="52ffd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="52ffd-123">Requirement</span></span> | <span data-ttu-id="52ffd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="52ffd-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ffd-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52ffd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="52ffd-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52ffd-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="52ffd-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52ffd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="52ffd-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52ffd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52ffd-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="52ffd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="52ffd-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52ffd-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ffd-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52ffd-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="52ffd-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="52ffd-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52ffd-133">**WM \_ чанжеуистате**</span><span class="sxs-lookup"><span data-stu-id="52ffd-133">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="52ffd-134">**WM \_ упдатеуистате**</span><span class="sxs-lookup"><span data-stu-id="52ffd-134">**WM\_UPDATEUISTATE**</span></span>](wm-updateuistate.md)
</dt> <dt>

<span data-ttu-id="52ffd-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="52ffd-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="52ffd-136">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="52ffd-136">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

 





