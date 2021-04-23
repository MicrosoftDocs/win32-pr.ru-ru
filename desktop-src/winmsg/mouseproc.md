---
UID: ''
title: Функция обратного вызова Маусепрок
description: Система вызывает эту функцию, когда приложение вызывает функцию сообщения и имеется сообщение, которое необходимо обработать.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "105700833"
---
# <a name="mouseproc-function"></a><span data-ttu-id="b5775-103">Функция Маусепрок</span><span class="sxs-lookup"><span data-stu-id="b5775-103">MouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="b5775-104">Описание</span><span class="sxs-lookup"><span data-stu-id="b5775-104">Description</span></span>

<span data-ttu-id="b5775-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="b5775-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="b5775-106">Система вызывает эту функцию всякий [раз, когда](/windows/desktop/api/winuser/nf-winuser-getmessage) приложение вызывает функцию [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) и для обработки сообщений мыши.</span><span class="sxs-lookup"><span data-stu-id="b5775-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a mouse message to be processed.</span></span>

<span data-ttu-id="b5775-107">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b5775-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="b5775-108">**Маусепрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="b5775-108">**MouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="b5775-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5775-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="b5775-110">Нкоде [in]</span><span class="sxs-lookup"><span data-stu-id="b5775-110">nCode [in]</span></span>

<span data-ttu-id="b5775-111">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="b5775-111">Type: **int**</span></span>

<span data-ttu-id="b5775-112">Код, используемый процедурой-обработчиком для определения способа обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5775-112">A code that the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="b5775-113">Если *нкоде* меньше нуля, процедура-обработчик должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="b5775-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="b5775-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="b5775-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="b5775-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b5775-115">Value</span></span> | <span data-ttu-id="b5775-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b5775-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="b5775-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="b5775-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="b5775-118">Параметры *wParam* и *lParam* содержат сведения о сообщении мыши.</span><span class="sxs-lookup"><span data-stu-id="b5775-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |
| <span data-ttu-id="b5775-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="b5775-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="b5775-120">Параметры *wParam* и *lParam* содержат сведения о сообщении мыши, а сообщение мыши не было удалено из очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="b5775-120">The *wParam* and *lParam* parameters contain information about a mouse message, and the mouse message has not been removed from the message queue.</span></span> <span data-ttu-id="b5775-121">(Приложение, именуемое функцией **PeekMessage** , с указанием флага **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="b5775-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="b5775-122">wParam [вход]</span><span class="sxs-lookup"><span data-stu-id="b5775-122">wParam [in]</span></span>

<span data-ttu-id="b5775-123">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="b5775-123">Type: **WPARAM**</span></span>

<span data-ttu-id="b5775-124">Идентификатор сообщения мыши.</span><span class="sxs-lookup"><span data-stu-id="b5775-124">The identifier of the mouse message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="b5775-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="b5775-125">lParam [in]</span></span>

<span data-ttu-id="b5775-126">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="b5775-126">Type: **LPARAM**</span></span>

<span data-ttu-id="b5775-127">Указатель на структуру [маусехукструкт](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .</span><span class="sxs-lookup"><span data-stu-id="b5775-127">A pointer to a [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="b5775-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5775-128">Returns</span></span>

<span data-ttu-id="b5775-129">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="b5775-129">Type: **LRESULT**</span></span>

<span data-ttu-id="b5775-130">Если *нкоде* меньше нуля, процедура-обработчик должна возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="b5775-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="b5775-131">Если *нкоде* больше или равен нулю и процедура обработчика не обработала сообщение, настоятельно рекомендуется вызвать метод **каллнекссукекс** и вернуть возвращаемое значение. в противном случае другие приложения, которые установили [WH_MOUSEные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.</span><span class="sxs-lookup"><span data-stu-id="b5775-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="b5775-132">Если процедура обработки сообщения обрабатывает сообщение, она может вернуть ненулевое значение, чтобы система не могла передать сообщение в целевую процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="b5775-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5775-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5775-133">Remarks</span></span>

<span data-ttu-id="b5775-134">Приложение устанавливает процедуру-обработчик, указывая тип обработчика WH_MOUSE и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="b5775-134">An application installs the hook procedure by specifying the WH_MOUSE hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="b5775-135">Процедура-обработчик не должна устанавливать [WH_JOURNALPLAYBACK](about-hooks.md) функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b5775-135">The hook procedure must not install a [WH_JOURNALPLAYBACK](about-hooks.md) callback function.</span></span>

<span data-ttu-id="b5775-136">Этот обработчик может быть вызван в контексте потока, установившего его.</span><span class="sxs-lookup"><span data-stu-id="b5775-136">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="b5775-137">Вызов осуществляется путем отправки сообщения в поток, устанавливающий обработчик.</span><span class="sxs-lookup"><span data-stu-id="b5775-137">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="b5775-138">Таким образом, поток, устанавливающий обработчик, должен иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="b5775-138">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5775-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5775-139">See also</span></span>

[<span data-ttu-id="b5775-140">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="b5775-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="b5775-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="b5775-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="b5775-142">маусехукструкт</span><span class="sxs-lookup"><span data-stu-id="b5775-142">MOUSEHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[<span data-ttu-id="b5775-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="b5775-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="b5775-144">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="b5775-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="b5775-145">Обработчики</span><span class="sxs-lookup"><span data-stu-id="b5775-145">Hooks</span></span>](hooks.md)

[<span data-ttu-id="b5775-146">О обработчиках</span><span class="sxs-lookup"><span data-stu-id="b5775-146">About Hooks</span></span>](about-hooks.md)
