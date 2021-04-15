---
description: Приложение отправляет \_ сообщение WM мдиресторе в окно клиента многодокументного интерфейса (MDI) для восстановления дочернего окна MDI из развернутого или минимального размера.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Сообщение WM_MDIRESTORE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701435"
---
# <a name="wm_mdirestore-message"></a><span data-ttu-id="6fc1f-103">\_Сообщение МДИРЕСТОРЕ WM</span><span class="sxs-lookup"><span data-stu-id="6fc1f-103">WM\_MDIRESTORE message</span></span>

<span data-ttu-id="6fc1f-104">Приложение отправляет сообщение **WM \_ мдиресторе** в окно клиента многодокументного интерфейса (MDI) для восстановления дочернего окна MDI из развернутого или минимального размера.</span><span class="sxs-lookup"><span data-stu-id="6fc1f-104">An application sends the **WM\_MDIRESTORE** message to a multiple-document interface (MDI) client window to restore an MDI child window from maximized or minimized size.</span></span>


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a><span data-ttu-id="6fc1f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fc1f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc1f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fc1f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fc1f-107">Описатель дочернего окна MDI, подлежащей восстановлению.</span><span class="sxs-lookup"><span data-stu-id="6fc1f-107">A handle to the MDI child window to be restored.</span></span>

</dd> <dt>

<span data-ttu-id="6fc1f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fc1f-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fc1f-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="6fc1f-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc1f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fc1f-110">Return value</span></span>

<span data-ttu-id="6fc1f-111">Тип: **ноль**</span><span class="sxs-lookup"><span data-stu-id="6fc1f-111">Type: **zero**</span></span>

<span data-ttu-id="6fc1f-112">Возвращаемое значение всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6fc1f-112">The return value is always zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc1f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6fc1f-113">Requirements</span></span>



| <span data-ttu-id="6fc1f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6fc1f-114">Requirement</span></span> | <span data-ttu-id="6fc1f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6fc1f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc1f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fc1f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc1f-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fc1f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6fc1f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fc1f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc1f-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fc1f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6fc1f-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6fc1f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc1f-121"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fc1f-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fc1f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fc1f-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="6fc1f-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6fc1f-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6fc1f-124">**WM \_ мдимаксимизе**</span><span class="sxs-lookup"><span data-stu-id="6fc1f-124">**WM\_MDIMAXIMIZE**</span></span>](wm-mdimaximize.md)
</dt> <dt>

<span data-ttu-id="6fc1f-125">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="6fc1f-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6fc1f-126">Интерфейс с несколькими документами</span><span class="sxs-lookup"><span data-stu-id="6fc1f-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




