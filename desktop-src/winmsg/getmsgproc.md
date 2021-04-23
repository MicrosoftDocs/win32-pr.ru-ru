---
UID: ''
title: Функция обратного вызова Жетмсгпрок
description: Система вызывает эту функцию, когда функция сообщения получает сообщение из очереди сообщений приложения.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "105691968"
---
# <a name="getmsgproc-function"></a><span data-ttu-id="5c530-103">Функция Жетмсгпрок</span><span class="sxs-lookup"><span data-stu-id="5c530-103">GetMsgProc function</span></span>

## <a name="-description"></a><span data-ttu-id="5c530-104">-Описание</span><span class="sxs-lookup"><span data-stu-id="5c530-104">-description</span></span>

<span data-ttu-id="5c530-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="5c530-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span> <span data-ttu-id="5c530-106">Система вызывает эту функцию при извлечении сообщения из очереди сообщений приложения функцией [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) или функции WITH [Message](/windows/desktop/api/winuser/nf-winuser-getmessage) .</span><span class="sxs-lookup"><span data-stu-id="5c530-106">The system calls this function whenever the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function has retrieved a message from an application message queue.</span></span>
<span data-ttu-id="5c530-107">Перед возвратом полученного сообщения вызывающему объекту система передает сообщение в процедуру-обработчик.</span><span class="sxs-lookup"><span data-stu-id="5c530-107">Before returning the retrieved message to the caller, the system passes the message to the hook procedure.</span></span>

<span data-ttu-id="5c530-108">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="5c530-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="5c530-109">**Жетмсгпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="5c530-109">**GetMsgProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a><span data-ttu-id="5c530-110">-Parameters</span><span class="sxs-lookup"><span data-stu-id="5c530-110">-parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="5c530-111">код [в]</span><span class="sxs-lookup"><span data-stu-id="5c530-111">code [in]</span></span>

<span data-ttu-id="5c530-112">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="5c530-112">Type: **int**</span></span>

<span data-ttu-id="5c530-113">Указывает, должна ли процедура-обработчик обработать сообщение.</span><span class="sxs-lookup"><span data-stu-id="5c530-113">Specifies whether the hook procedure must process the message.</span></span>
<span data-ttu-id="5c530-114">Если *код* **HC_ACTION**, процедура обработчика должна обработать сообщение.</span><span class="sxs-lookup"><span data-stu-id="5c530-114">If *code* is **HC_ACTION**, the hook procedure must process the message.</span></span>
<span data-ttu-id="5c530-115">Если *код* меньше нуля, процедура обработчика должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="5c530-115">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>

### <a name="wparam-in"></a><span data-ttu-id="5c530-116">wParam [вход]</span><span class="sxs-lookup"><span data-stu-id="5c530-116">wParam [in]</span></span>

<span data-ttu-id="5c530-117">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="5c530-117">Type: **WPARAM**</span></span>

<span data-ttu-id="5c530-118">Указывает, было ли сообщение удалено из очереди.</span><span class="sxs-lookup"><span data-stu-id="5c530-118">Specifies whether the message has been removed from the queue.</span></span>
<span data-ttu-id="5c530-119">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="5c530-119">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="5c530-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5c530-120">Value</span></span> | <span data-ttu-id="5c530-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5c530-121">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="5c530-122">**PM_NOREMOVE** Символ 0x0000</span><span class="sxs-lookup"><span data-stu-id="5c530-122">**PM_NOREMOVE** 0x0000</span></span> | <span data-ttu-id="5c530-123">Сообщение не было удалено из очереди.</span><span class="sxs-lookup"><span data-stu-id="5c530-123">The message has not been removed from the queue.</span></span> <span data-ttu-id="5c530-124">(Приложение, именуемое функцией **PeekMessage** , с указанием флага **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="5c530-124">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |
| <span data-ttu-id="5c530-125">**PM_REMOVE** 0x0001</span><span class="sxs-lookup"><span data-stu-id="5c530-125">**PM_REMOVE** 0x0001</span></span> | <span data-ttu-id="5c530-126">Сообщение было удалено из очереди.</span><span class="sxs-lookup"><span data-stu-id="5c530-126">The message has been removed from the queue.</span></span> <span data-ttu-id="5c530-127">(Приложение **с именем или** функцией  **PeekMessage** , которое указывает флаг **PM_REMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="5c530-127">(An application called **GetMessage**, or it called the  **PeekMessage** function, specifying the **PM_REMOVE** flag.)</span></span>|

### <a name="lparam-in"></a><span data-ttu-id="5c530-128">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="5c530-128">lParam [in]</span></span>

<span data-ttu-id="5c530-129">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="5c530-129">Type: **LPARAM**</span></span>

<span data-ttu-id="5c530-130">Указатель на структуру [MSG](/windows/desktop/api/winuser/ns-winuser-msg) , содержащую сведения о сообщении.</span><span class="sxs-lookup"><span data-stu-id="5c530-130">A pointer to an [MSG](/windows/desktop/api/winuser/ns-winuser-msg) structure that contains details about the message.</span></span>

## <a name="-returns"></a><span data-ttu-id="5c530-131">— Возвращает</span><span class="sxs-lookup"><span data-stu-id="5c530-131">-returns</span></span>

<span data-ttu-id="5c530-132">Если *код* меньше нуля, процедура обработчика должна возвращать значение, возвращаемое функцией [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span><span class="sxs-lookup"><span data-stu-id="5c530-132">If *code* is less than zero, the hook procedure must return the value returned by [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="5c530-133">Если *код* больше или равен нулю, настоятельно рекомендуется вызвать **каллнекссукекс** и возвратить возвращаемое значение. в противном случае другие приложения, которые установили [WH_GETMESSAGEные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.</span><span class="sxs-lookup"><span data-stu-id="5c530-133">If *code* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_GETMESSAGE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="5c530-134">Если процедура-обработчик не вызывает **каллнекссукекс**, возвращаемое значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5c530-134">If the hook procedure does not call **CallNextHookEx**, the return value should be zero.</span></span>

## <a name="-remarks"></a><span data-ttu-id="5c530-135">-замечания</span><span class="sxs-lookup"><span data-stu-id="5c530-135">-remarks</span></span>

<span data-ttu-id="5c530-136">Процедура-обработчик **жетмсгпрок** может проверить или изменить сообщение.</span><span class="sxs-lookup"><span data-stu-id="5c530-136">The **GetMsgProc** hook procedure can examine or modify the message.</span></span>
<span data-ttu-id="5c530-137">После того как процедура-обработчик возвращает управление системе, функция **PeekMessage** и **Message** , а также любые изменения передаются в приложение, которое его вызвало.</span><span class="sxs-lookup"><span data-stu-id="5c530-137">After the hook procedure returns control to the system, the **GetMessage** or **PeekMessage** function returns the message, along with any modifications, to the application that originally called it.</span></span>

<span data-ttu-id="5c530-138">Приложение устанавливает эту процедуру-обработчик, указывая тип обработчика **WH_GETMESSAGE** и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="5c530-138">An application installs this hook procedure by specifying the **WH_GETMESSAGE** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c530-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c530-139">See also</span></span>

[<span data-ttu-id="5c530-140">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="5c530-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="5c530-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="5c530-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="5c530-142">ОБ</span><span class="sxs-lookup"><span data-stu-id="5c530-142">MSG</span></span>](/windows/desktop/api/winuser/ns-winuser-msg)

[<span data-ttu-id="5c530-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="5c530-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="5c530-144">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="5c530-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="5c530-145">Обработчики</span><span class="sxs-lookup"><span data-stu-id="5c530-145">Hooks</span></span>](hooks.md)
