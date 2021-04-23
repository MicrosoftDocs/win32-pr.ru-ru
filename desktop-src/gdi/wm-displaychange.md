---
description: Сообщение WM \_ дисплайчанже отправляется всем окнам при изменении разрешения экрана.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Сообщение WM_DISPLAYCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264121"
---
# <a name="wm_displaychange-message"></a><span data-ttu-id="babec-103">\_Сообщение ДИСПЛАЙЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="babec-103">WM\_DISPLAYCHANGE message</span></span>

<span data-ttu-id="babec-104">Сообщение **WM \_ дисплайчанже** отправляется всем окнам при изменении разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="babec-104">The **WM\_DISPLAYCHANGE** message is sent to all windows when the display resolution has changed.</span></span>

<span data-ttu-id="babec-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="babec-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="babec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="babec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="babec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="babec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="babec-108">Новая глубина изображения для дисплея в битах на пиксель.</span><span class="sxs-lookup"><span data-stu-id="babec-108">The new image depth of the display, in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="babec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="babec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="babec-110">Слово нижнего порядка задает горизонтальное разрешение экрана.</span><span class="sxs-lookup"><span data-stu-id="babec-110">The low-order word specifies the horizontal resolution of the screen.</span></span>

<span data-ttu-id="babec-111">Слово в высоком порядке указывает вертикальное разрешение экрана.</span><span class="sxs-lookup"><span data-stu-id="babec-111">The high-order word specifies the vertical resolution of the screen.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="babec-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="babec-112">Remarks</span></span>

<span data-ttu-id="babec-113">Это сообщение отправляется только в окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="babec-113">This message is only sent to top-level windows.</span></span> <span data-ttu-id="babec-114">Для всех остальных окон, которые он публикует.</span><span class="sxs-lookup"><span data-stu-id="babec-114">For all other windows it is posted.</span></span>

## <a name="requirements"></a><span data-ttu-id="babec-115">Требования</span><span class="sxs-lookup"><span data-stu-id="babec-115">Requirements</span></span>



| <span data-ttu-id="babec-116">Требование</span><span class="sxs-lookup"><span data-stu-id="babec-116">Requirement</span></span> | <span data-ttu-id="babec-117">Значение</span><span class="sxs-lookup"><span data-stu-id="babec-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="babec-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="babec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="babec-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="babec-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="babec-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="babec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="babec-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="babec-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="babec-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="babec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="babec-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="babec-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="babec-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="babec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="babec-125">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="babec-125">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="babec-126">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="babec-126">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

<span data-ttu-id="babec-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="babec-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="babec-128">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="babec-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

 
