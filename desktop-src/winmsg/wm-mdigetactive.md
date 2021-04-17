---
description: Приложение отправляет \_ сообщение WM мдижетактиве в окно клиента многодокументного интерфейса (MDI) для получения маркера в активное дочернее окно MDI.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Сообщение WM_MDIGETACTIVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702571"
---
# <a name="wm_mdigetactive-message"></a><span data-ttu-id="b6bb6-103">\_Сообщение МДИЖЕТАКТИВЕ WM</span><span class="sxs-lookup"><span data-stu-id="b6bb6-103">WM\_MDIGETACTIVE message</span></span>

<span data-ttu-id="b6bb6-104">Приложение отправляет сообщение **WM \_ мдижетактиве** в окно клиента многодокументного интерфейса (MDI) для получения маркера в активное дочернее окно MDI.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-104">An application sends the **WM\_MDIGETACTIVE** message to a multiple-document interface (MDI) client window to retrieve the handle to the active MDI child window.</span></span>


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a><span data-ttu-id="b6bb6-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6bb6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6bb6-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6bb6-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6bb6-107">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6bb6-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6bb6-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6bb6-109">Развернутое состояние.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-109">The maximized state.</span></span> <span data-ttu-id="b6bb6-110">Если этот параметр не равен **null**, это указатель на значение, указывающее развернутое состояние дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-110">If this parameter is not **NULL**, it is a pointer to a value that indicates the maximized state of the MDI child window.</span></span> <span data-ttu-id="b6bb6-111">Если значение равно **true**, окно разворачивается. значение **false** указывает, что это не так.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-111">If the value is **TRUE**, the window is maximized; a value of **FALSE** indicates that it is not.</span></span> <span data-ttu-id="b6bb6-112">Если этот параметр имеет **значение NULL**, параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-112">If this parameter is **NULL**, the parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6bb6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6bb6-113">Return value</span></span>

<span data-ttu-id="b6bb6-114">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="b6bb6-114">Type: **HWND**</span></span>

<span data-ttu-id="b6bb6-115">Возвращаемое значение — это маркер активного дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-115">The return value is the handle to the active MDI child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bb6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b6bb6-116">Requirements</span></span>



| <span data-ttu-id="b6bb6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b6bb6-117">Requirement</span></span> | <span data-ttu-id="b6bb6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b6bb6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bb6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6bb6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6bb6-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6bb6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b6bb6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6bb6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6bb6-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6bb6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6bb6-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6bb6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6bb6-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb6-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6bb6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6bb6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6bb6-126">Общие сведения об интерфейсе нескольких документов</span><span class="sxs-lookup"><span data-stu-id="b6bb6-126">Multiple Document Interface Overview</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




