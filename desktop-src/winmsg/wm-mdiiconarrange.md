---
description: Приложение отправляет \_ сообщение WM мдииконарранже в окно клиента многодокументного интерфейса (MDI) для упорядочения всех минимальных дочерних окон MDI. Он не влияет на несведенные дочерние окна.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Сообщение WM_MDIICONARRANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497319"
---
# <a name="wm_mdiiconarrange-message"></a><span data-ttu-id="c779d-104">\_Сообщение МДИИКОНАРРАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="c779d-104">WM\_MDIICONARRANGE message</span></span>

<span data-ttu-id="c779d-105">Приложение отправляет сообщение **WM \_ мдииконарранже** в окно клиента многодокументного интерфейса (MDI) для упорядочения всех минимальных дочерних окон MDI.</span><span class="sxs-lookup"><span data-stu-id="c779d-105">An application sends the **WM\_MDIICONARRANGE** message to a multiple-document interface (MDI) client window to arrange all minimized MDI child windows.</span></span> <span data-ttu-id="c779d-106">Он не влияет на несведенные дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="c779d-106">It does not affect child windows that are not minimized.</span></span>


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a><span data-ttu-id="c779d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c779d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c779d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c779d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c779d-109">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c779d-109">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c779d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c779d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c779d-111">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c779d-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c779d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c779d-112">Requirements</span></span>



| <span data-ttu-id="c779d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c779d-113">Requirement</span></span> | <span data-ttu-id="c779d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c779d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c779d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c779d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c779d-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c779d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c779d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c779d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c779d-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c779d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c779d-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c779d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c779d-120"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c779d-120"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c779d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c779d-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="c779d-122">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c779d-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c779d-123">**WM \_ мдикаскаде**</span><span class="sxs-lookup"><span data-stu-id="c779d-123">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="c779d-124">**WM \_ мдитиле**</span><span class="sxs-lookup"><span data-stu-id="c779d-124">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="c779d-125">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c779d-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c779d-126">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="c779d-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




