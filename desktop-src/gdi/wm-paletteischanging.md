---
description: Сообщение WM \_ палеттеисчангинг информирует приложения о том, что приложение будет реализовывать логическую палитру.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Сообщение WM_PALETTEISCHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815528"
---
# <a name="wm_paletteischanging-message"></a><span data-ttu-id="63102-103">\_Сообщение ПАЛЕТТЕИСЧАНГИНГ WM</span><span class="sxs-lookup"><span data-stu-id="63102-103">WM\_PALETTEISCHANGING message</span></span>

<span data-ttu-id="63102-104">Сообщение **WM \_ палеттеисчангинг** информирует приложения о том, что приложение будет реализовывать логическую палитру.</span><span class="sxs-lookup"><span data-stu-id="63102-104">The **WM\_PALETTEISCHANGING** message informs applications that an application is going to realize its logical palette.</span></span>

<span data-ttu-id="63102-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="63102-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="63102-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63102-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63102-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63102-108">Маркер окна, который будет реализовывать свою логическую палитру.</span><span class="sxs-lookup"><span data-stu-id="63102-108">A handle to the window that is going to realize its logical palette.</span></span>

</dd> <dt>

<span data-ttu-id="63102-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63102-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63102-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="63102-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63102-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63102-111">Return value</span></span>

<span data-ttu-id="63102-112">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="63102-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="63102-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="63102-113">Remarks</span></span>

<span data-ttu-id="63102-114">Приложение, изменяющее палитру, не ждет подтверждения этого сообщения перед изменением палитры и отправкой сообщения [**WM \_ палеттечанжед**](wm-palettechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="63102-114">The application changing its palette does not wait for acknowledgment of this message before changing the palette and sending the [**WM\_PALETTECHANGED**](wm-palettechanged.md) message.</span></span> <span data-ttu-id="63102-115">В результате эта палитра может быть уже изменена временем, когда приложение получает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="63102-115">As a result, the palette may already be changed by the time an application receives this message.</span></span>

<span data-ttu-id="63102-116">Если приложение пропускает или не обрабатывает это сообщение, а второе приложение понимает его палитру, а первое использует индексы палитры, существует строгая вероятность того, что пользователь увидит непредвиденные цвета во время последующих операций рисования.</span><span class="sxs-lookup"><span data-stu-id="63102-116">If the application either ignores or fails to process this message and a second application realizes its palette while the first is using palette indexes, there is a strong possibility that the user will see unexpected colors during subsequent drawing operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="63102-117">Требования</span><span class="sxs-lookup"><span data-stu-id="63102-117">Requirements</span></span>



| <span data-ttu-id="63102-118">Требование</span><span class="sxs-lookup"><span data-stu-id="63102-118">Requirement</span></span> | <span data-ttu-id="63102-119">Значение</span><span class="sxs-lookup"><span data-stu-id="63102-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63102-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63102-120">Minimum supported client</span></span><br/> | <span data-ttu-id="63102-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63102-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="63102-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63102-122">Minimum supported server</span></span><br/> | <span data-ttu-id="63102-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63102-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63102-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="63102-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="63102-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63102-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63102-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63102-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63102-127">Общие сведения о цветах</span><span class="sxs-lookup"><span data-stu-id="63102-127">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="63102-128">Цветные сообщения</span><span class="sxs-lookup"><span data-stu-id="63102-128">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="63102-129">**WM \_ палеттечанжед**</span><span class="sxs-lookup"><span data-stu-id="63102-129">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="63102-130">**WM \_ куериневпалетте**</span><span class="sxs-lookup"><span data-stu-id="63102-130">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
