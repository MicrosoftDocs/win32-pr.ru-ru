---
description: Приложение отправляет \_ сообщение WM мдитиле в окно клиента многодокументного интерфейса (MDI) для упорядочения всех своих дочерних окон MDI в формате мозаики.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Сообщение WM_MDITILE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263023"
---
# <a name="wm_mditile-message"></a><span data-ttu-id="f7988-103">\_Сообщение МДИТИЛЕ WM</span><span class="sxs-lookup"><span data-stu-id="f7988-103">WM\_MDITILE message</span></span>

<span data-ttu-id="f7988-104">Приложение отправляет сообщение **WM \_ мдитиле** в окно клиента многодокументного интерфейса (MDI) для упорядочения всех своих дочерних окон MDI в формате мозаики.</span><span class="sxs-lookup"><span data-stu-id="f7988-104">An application sends the **WM\_MDITILE** message to a multiple-document interface (MDI) client window to arrange all of its MDI child windows in a tile format.</span></span>


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a><span data-ttu-id="f7988-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7988-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7988-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7988-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7988-107">Параметр мозаичного заполнения.</span><span class="sxs-lookup"><span data-stu-id="f7988-107">The tiling option.</span></span> <span data-ttu-id="f7988-108">Этот параметр может принимать одно из следующих значений, при необходимости сочетающийся с **мдитиле \_ скипдисаблед** , чтобы отключить мозаичное заполнение отключенных дочерних окон MDI.</span><span class="sxs-lookup"><span data-stu-id="f7988-108">This parameter can be one of the following values, optionally combined with **MDITILE\_SKIPDISABLED** to prevent disabled MDI child windows from being tiled.</span></span>



| <span data-ttu-id="f7988-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f7988-109">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="f7988-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f7988-110">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <span data-ttu-id="f7988-111"><dt>**Мдитиле \_ ГОРИЗОНТАЛЬное**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f7988-111"><dt>**MDITILE\_HORIZONTAL**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="f7988-112">Окна мозаики по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="f7988-112">Tiles windows horizontally.</span></span><br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <span data-ttu-id="f7988-113"><dt>**Мдитиле \_ ВЕРТИКАЛЬный**</dt> <dt>Символ 0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="f7988-113"><dt>**MDITILE\_VERTICAL**</dt> <dt>0x0000</dt></span></span> </dl>       | <span data-ttu-id="f7988-114">Окна мозаики по вертикали.</span><span class="sxs-lookup"><span data-stu-id="f7988-114">Tiles windows vertically.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f7988-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7988-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7988-116">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="f7988-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7988-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7988-117">Return value</span></span>

<span data-ttu-id="f7988-118">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="f7988-118">Type: **BOOL**</span></span>

<span data-ttu-id="f7988-119">Если сообщение прошло удачно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="f7988-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="f7988-120">Если сообщение не выполняется, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="f7988-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7988-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f7988-121">Requirements</span></span>



| <span data-ttu-id="f7988-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f7988-122">Requirement</span></span> | <span data-ttu-id="f7988-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f7988-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7988-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7988-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7988-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f7988-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f7988-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7988-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7988-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f7988-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7988-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f7988-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7988-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7988-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7988-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7988-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7988-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f7988-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7988-132">**WM \_ мдикаскаде**</span><span class="sxs-lookup"><span data-stu-id="f7988-132">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="f7988-133">**WM \_ мдииконарранже**</span><span class="sxs-lookup"><span data-stu-id="f7988-133">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

<span data-ttu-id="f7988-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f7988-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f7988-135">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="f7988-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




