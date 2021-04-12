---
title: Код уведомления EN_SEARCHWEB (Коммктрл. h)
description: Посылается, когда элемент управления "поле ввода" теряет фокус клавиатуры. Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ сообщение уведомления WM.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489279"
---
# <a name="en_searchweb-notification-code"></a><span data-ttu-id="60dc4-105">\_Код уведомления EN сеарчвеб</span><span class="sxs-lookup"><span data-stu-id="60dc4-105">EN\_SEARCHWEB notification code</span></span>

<span data-ttu-id="60dc4-106">Посылается после того, как элемент управления "поле ввода" выполнил Поиск в Интернете при включении функции "Поиск в Интернете", см. статью [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span><span class="sxs-lookup"><span data-stu-id="60dc4-106">Sent after an edit control performed a web search when the "Search the web" feature is enabled, see [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span></span> <span data-ttu-id="60dc4-107">Родительское окно элемента управления "поле ввода" получает этот код уведомления через сообщение [**\_ уведомления WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="60dc4-107">The parent window of the edit control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="60dc4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60dc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60dc4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60dc4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60dc4-110">Обработчик для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="60dc4-110">Handle to the edit control.</span></span>

</dd> <dt>

<span data-ttu-id="60dc4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60dc4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60dc4-112">Указатель на структуру [**нмсеарчвеб**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .</span><span class="sxs-lookup"><span data-stu-id="60dc4-112">A pointer to a [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60dc4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="60dc4-113">Requirements</span></span>



| <span data-ttu-id="60dc4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="60dc4-114">Requirement</span></span> | <span data-ttu-id="60dc4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="60dc4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60dc4-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60dc4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60dc4-117">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="60dc4-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="60dc4-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60dc4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60dc4-119">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="60dc4-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="60dc4-120">Header</span><span class="sxs-lookup"><span data-stu-id="60dc4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60dc4-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="60dc4-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60dc4-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60dc4-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="60dc4-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="60dc4-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="60dc4-124">**EM \_ енаблесеарчвеб**</span><span class="sxs-lookup"><span data-stu-id="60dc4-124">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> <dt>

<span data-ttu-id="60dc4-125">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="60dc4-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="60dc4-126">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="60dc4-126">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





