---
description: Приложение отправляет \_ сообщение WM мдикаскаде в окно клиента многодокументного интерфейса (MDI) для упорядочения всех его дочерних окон в каскадном формате.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Сообщение WM_MDICASCADE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343202"
---
# <a name="wm_mdicascade-message"></a><span data-ttu-id="fc1c2-103">\_Сообщение МДИКАСКАДЕ WM</span><span class="sxs-lookup"><span data-stu-id="fc1c2-103">WM\_MDICASCADE message</span></span>

<span data-ttu-id="fc1c2-104">Приложение отправляет сообщение **WM \_ мдикаскаде** в окно клиента многодокументного интерфейса (MDI) для упорядочения всех его дочерних окон в каскадном формате.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-104">An application sends the **WM\_MDICASCADE** message to a multiple-document interface (MDI) client window to arrange all its child windows in a cascade format.</span></span>


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a><span data-ttu-id="fc1c2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc1c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc1c2-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc1c2-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc1c2-107">Поведение Cascade.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-107">The cascade behavior.</span></span> <span data-ttu-id="fc1c2-108">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-108">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="fc1c2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="fc1c2-109">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="fc1c2-110">Значение</span><span class="sxs-lookup"><span data-stu-id="fc1c2-110">Meaning</span></span>                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <span data-ttu-id="fc1c2-111"><dt>**Мдитиле \_ СКИПДИСАБЛЕД**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="fc1c2-111"><dt>**MDITILE\_SKIPDISABLED**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="fc1c2-112">Запрещает каскадное отображение отключенных дочерних окон MDI.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-112">Prevents disabled MDI child windows from being cascaded.</span></span> <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <span data-ttu-id="fc1c2-113"><dt>**Мдитиле \_ ЗОРДЕР**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="fc1c2-113"><dt>**MDITILE\_ZORDER**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="fc1c2-114">Упорядочивает окна в Z порядке.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-114">Arranges the windows in Z order.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="fc1c2-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc1c2-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc1c2-116">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc1c2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc1c2-117">Return value</span></span>

<span data-ttu-id="fc1c2-118">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="fc1c2-118">Type: **BOOL**</span></span>

<span data-ttu-id="fc1c2-119">Если сообщение прошло удачно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="fc1c2-120">Если сообщение не выполняется, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="fc1c2-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1c2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fc1c2-121">Requirements</span></span>



| <span data-ttu-id="fc1c2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fc1c2-122">Requirement</span></span> | <span data-ttu-id="fc1c2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fc1c2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1c2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc1c2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1c2-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc1c2-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fc1c2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc1c2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1c2-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc1c2-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc1c2-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc1c2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc1c2-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc1c2-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc1c2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc1c2-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc1c2-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fc1c2-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fc1c2-132">**WM \_ мдииконарранже**</span><span class="sxs-lookup"><span data-stu-id="fc1c2-132">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

[<span data-ttu-id="fc1c2-133">**WM \_ мдитиле**</span><span class="sxs-lookup"><span data-stu-id="fc1c2-133">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="fc1c2-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fc1c2-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fc1c2-135">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="fc1c2-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




