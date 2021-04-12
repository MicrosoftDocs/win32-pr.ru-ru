---
title: Сообщение WM_DDE_INITIATE (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение запуска WM DDE для инициации диалога с серверным приложением, отвечающим на указанные имена приложений и разделов.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- Обмен данными с сообщениями WM_DDE_INITIATE
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415393"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="5c8ba-104">\_ \_ Сообщение об инициации DDE в WM</span><span class="sxs-lookup"><span data-stu-id="5c8ba-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="5c8ba-105">Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **\_ \_ запуска WM DDE** для инициации диалога с серверным приложением, отвечающим на указанные имена приложений и разделов.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="5c8ba-106">После получения этого сообщения все серверные приложения с именами, которые соответствуют указанному приложению и поддерживают указанный раздел, должны подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="5c8ba-107">(Дополнительные сведения см. в описании сообщения [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .)</span><span class="sxs-lookup"><span data-stu-id="5c8ba-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="5c8ba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c8ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c8ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c8ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c8ba-110">Маркер клиентского окна, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="5c8ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c8ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c8ba-112">Слово нижнего порядка содержит объект Atom, определяющий приложение, с которым запрашивается диалог.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="5c8ba-113">Имя приложения не может содержать символы косой черты (/) или обратные косые черты ( \) .</span><span class="sxs-lookup"><span data-stu-id="5c8ba-113">The application name cannot contain slashes (/) or backslashes (\).</span></span> <span data-ttu-id="5c8ba-114">Эти символы зарезервированы для реализации сети.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="5c8ba-115">Если этот параметр имеет **значение NULL**, запрашивается диалог со всеми приложениями.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="5c8ba-116">Слово с высоким порядком содержит объект Atom, который определяет тему, для которой запрашивается диалог.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="5c8ba-117">Если раздел имеет **значение NULL**, запрашиваются все доступные разделы.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c8ba-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c8ba-118">Remarks</span></span>

<span data-ttu-id="5c8ba-119">Если неупорядоченное слово *lParam* имеет **значение NULL**, любое серверное приложение может ответить.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="5c8ba-120">Если слово *lParam* с высоким приоритетом имеет **значение NULL**, любой раздел является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="5c8ba-121">При получении запроса **на \_ \_ Запуск приложения WM DDE** с помощью слова с высоким порядковым значением параметра *lParam* , установленного в **значение NULL**, сервер должен отправить сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для каждого поддерживаемого раздела.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="5c8ba-122">Отправка</span><span class="sxs-lookup"><span data-stu-id="5c8ba-122">Sending</span></span>

<span data-ttu-id="5c8ba-123">Клиент передает сообщение всем окнам верхнего уровня, присвоив первому параметру [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) значение **HWND \_ Broadcast**.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="5c8ba-124">Если клиентское приложение уже получило обработчик окна нужного сервера, оно может отправить **WM \_ \_ DDE** в окно сервера, передав его в качестве первого параметра [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)в окне сервера.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="5c8ba-125">Клиентское приложение выделяет атомы, вызывая функцию [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="5c8ba-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="5c8ba-126">Когда [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) возвращает, клиентское приложение должно удалить атомы.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="5c8ba-127">Получение</span><span class="sxs-lookup"><span data-stu-id="5c8ba-127">Receiving</span></span>

<span data-ttu-id="5c8ba-128">Чтобы завершить инициацию диалога, серверное приложение должно ответить одним или несколькими сообщениями [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , где каждое сообщение предназначено для отдельного раздела.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="5c8ba-129">При отправке сообщения **WM \_ DDE \_ ACK** сервер должен создать новые атомы; он не должен повторно использовать атомы, отправленные с помощью **WM \_ DDE \_**.</span><span class="sxs-lookup"><span data-stu-id="5c8ba-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8ba-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5c8ba-130">Requirements</span></span>



| <span data-ttu-id="5c8ba-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5c8ba-131">Requirement</span></span> | <span data-ttu-id="5c8ba-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5c8ba-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8ba-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c8ba-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5c8ba-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c8ba-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5c8ba-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c8ba-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5c8ba-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c8ba-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5c8ba-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5c8ba-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c8ba-138"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c8ba-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8ba-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c8ba-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c8ba-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5c8ba-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c8ba-141">**глобаладдатом**</span><span class="sxs-lookup"><span data-stu-id="5c8ba-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="5c8ba-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="5c8ba-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="5c8ba-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="5c8ba-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="5c8ba-144">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="5c8ba-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="5c8ba-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5c8ba-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c8ba-146">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="5c8ba-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

