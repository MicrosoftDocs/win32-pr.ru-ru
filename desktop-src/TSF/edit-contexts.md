---
title: Изменение контекстов
description: Изменение контекстов
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Платформа текстовых служб (TSF), контекст правки
- TSF (платформа текстовых служб), контекст правки
- текстовые службы, контексты редактирования
- Приложения с поддержкой TSF, контексты изменения
- изменение контекстов
- Платформа текстовых служб (TSF), изменение файлов cookie
- TSF (платформа текстовых служб), изменение файлов cookie
- текстовые службы, изменение файлов cookie
- Приложения с поддержкой TSF, изменение файлов cookie
- изменить файлы cookie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888179"
---
# <a name="edit-contexts"></a><span data-ttu-id="80b5d-113">Изменение контекстов</span><span class="sxs-lookup"><span data-stu-id="80b5d-113">Edit Contexts</span></span>

## <a name="applications"></a><span data-ttu-id="80b5d-114">Приложения</span><span class="sxs-lookup"><span data-stu-id="80b5d-114">Applications</span></span>

<span data-ttu-id="80b5d-115">Чтобы создать контекст редактирования, приложение вызывает [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="80b5d-115">To create an edit context, an application calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>

## <a name="text-services"></a><span data-ttu-id="80b5d-116">Текстовые службы</span><span class="sxs-lookup"><span data-stu-id="80b5d-116">Text Services</span></span>

<span data-ttu-id="80b5d-117">В текстовой службе часто используется текущий активный контекст редактирования.</span><span class="sxs-lookup"><span data-stu-id="80b5d-117">A text service often uses the currently active edit context.</span></span> <span data-ttu-id="80b5d-118">Текущий активный контекст редактирования — это контекст редактирования в верхней части стека активного диспетчера документов.</span><span class="sxs-lookup"><span data-stu-id="80b5d-118">The currently active edit context is the edit context at the top of the stack of the active document manager.</span></span> <span data-ttu-id="80b5d-119">Чтобы получить текущий активный контекст, служба текстового ввода вызывает [ITfThreadMgr:: Focus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) для получения активного диспетчера документов, а затем вызывает [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) , чтобы получить контекст редактирования в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="80b5d-119">To obtain the currently active context, a text service calls [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) to obtain the active document manager and then calls [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) to obtain the edit context at the top of the stack.</span></span>

<span data-ttu-id="80b5d-120">В некоторых случаях для текстового сервиса требуется собственный контекст редактирования.</span><span class="sxs-lookup"><span data-stu-id="80b5d-120">In some cases, a text service requires its own edit context.</span></span> <span data-ttu-id="80b5d-121">Для создания контекста редактирования текстовая служба вызывает **ITfDocumentMgr:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="80b5d-121">To create an edit context, a text service calls **ITfDocumentMgr::CreateContext**.</span></span>

## <a name="edit-cookies"></a><span data-ttu-id="80b5d-122">Изменить файлы cookie</span><span class="sxs-lookup"><span data-stu-id="80b5d-122">Edit Cookies</span></span>

<span data-ttu-id="80b5d-123">Многие методы, такие как [итфранже:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), нуждаются в способе указать контекст редактирования, который имеет [блокировку документа](document-locks.md)только для чтения или чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="80b5d-123">Many methods, such as [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), require a way to identify an edit context that has a read-only or read/write [document lock](document-locks.md).</span></span> <span data-ttu-id="80b5d-124">Блокировка документа достигается за счет согласования между диспетчером TSF и приложением.</span><span class="sxs-lookup"><span data-stu-id="80b5d-124">A document lock is obtained through a negotiation between the TSF manager and the application.</span></span> <span data-ttu-id="80b5d-125">Служба текстового ввода не может выполнить это согласование напрямую.</span><span class="sxs-lookup"><span data-stu-id="80b5d-125">A text service cannot perform this negotiation directly.</span></span> <span data-ttu-id="80b5d-126">Служба текстового ввода может получить блокировку, запрашивая [сеанс редактирования](edit-sessions.md) с конкретным контекстом и доступом только для чтения или чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="80b5d-126">A text service can only obtain a lock by requesting an [edit session](edit-sessions.md) with a specific context and read-only or read/write access.</span></span> <span data-ttu-id="80b5d-127">При предоставлении сеанса редактирования текстовая служба получает *файл cookie редактирования* , который определяет контекст редактирования с запрошенным доступом.</span><span class="sxs-lookup"><span data-stu-id="80b5d-127">When the edit session is granted, the text service is supplied with an *edit cookie* that identifies the edit context with the requested access.</span></span> <span data-ttu-id="80b5d-128">Затем этот файл cookie передается в метод для обнаружения контекста редактирования с правильным доступом.</span><span class="sxs-lookup"><span data-stu-id="80b5d-128">This cookie is then passed to the method to identify the edit context with the proper access.</span></span>

<span data-ttu-id="80b5d-129">**ITfDocumentMgr:: CreateContext** также предоставляет файл cookie редактирования для создателя контекста.</span><span class="sxs-lookup"><span data-stu-id="80b5d-129">**ITfDocumentMgr::CreateContext** also supplies an edit cookie to the context creator.</span></span> <span data-ttu-id="80b5d-130">Этот файл cookie имеет доступ только для чтения, и изменить уровень доступа невозможно.</span><span class="sxs-lookup"><span data-stu-id="80b5d-130">This cookie has read-only access and there is no way to modify the access level.</span></span> <span data-ttu-id="80b5d-131">В действительности, диспетчер TSF не согласовывает блокировку документа для этого файла редактирования.</span><span class="sxs-lookup"><span data-stu-id="80b5d-131">In truth, the TSF manager does not negotiate a document lock for this edit cookie.</span></span> <span data-ttu-id="80b5d-132">Файл cookie внутренне помечен как "только для чтения", но документ фактически не блокируется.</span><span class="sxs-lookup"><span data-stu-id="80b5d-132">The cookie is internally marked read-only, but the document is not actually locked.</span></span> <span data-ttu-id="80b5d-133">Например, если создатель контекста вызывает [ITfContext::-SELECT](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) с изменением cookie, возвращенным **ITfDocumentMgr:: CreateContext** , это приводит к вызову [ITextStoreACP::-SELECT](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) или [итекстстореанчор::-SELECT](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) .</span><span class="sxs-lookup"><span data-stu-id="80b5d-133">For example, if the context creator calls [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) with the edit cookie returned by **ITfDocumentMgr::CreateContext** , this results in the application's [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) or [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) being called.</span></span> <span data-ttu-id="80b5d-134">Перед получением выбора приложение определит, существует ли блокировка документа.</span><span class="sxs-lookup"><span data-stu-id="80b5d-134">Before obtaining the selection, the application will determine if a document lock exists.</span></span> <span data-ttu-id="80b5d-135">Так как блокировка не существует, приложение завершится ошибкой с помощью TS \_ E \_ Lock.</span><span class="sxs-lookup"><span data-stu-id="80b5d-135">Because no lock exists, the application will fail with TS\_E\_NOLOCK.</span></span> <span data-ttu-id="80b5d-136">Это означает, что если приложение вызывает метод с этим файлом cookie, который приводит к вызову одного из методов хранилища текста приложения, он должен обработать этот случай, поскольку приложение на самом деле не будет блокировать документ.</span><span class="sxs-lookup"><span data-stu-id="80b5d-136">That is, if an application calls a method with this cookie that results in one of the application's text store methods being called, it must handle this case internally because the application will not actually have a document lock.</span></span>

<span data-ttu-id="80b5d-137">Если автору контекста требуется изменить файл cookie с доступом на чтение и запись, он должен установить собственный сеанс редактирования.</span><span class="sxs-lookup"><span data-stu-id="80b5d-137">If the context creator requires an edit cookie with read/write access, it must establish its own edit session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80b5d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="80b5d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80b5d-139">ITfContext</span><span class="sxs-lookup"><span data-stu-id="80b5d-139">ITfContext</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[<span data-ttu-id="80b5d-140">ITfDocumentMgr:: CreateContext</span><span class="sxs-lookup"><span data-stu-id="80b5d-140">ITfDocumentMgr::CreateContext</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="80b5d-141">ITfThreadMgr:: Focus</span><span class="sxs-lookup"><span data-stu-id="80b5d-141">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[<span data-ttu-id="80b5d-142">ITfDocumentMgr:: GetTop</span><span class="sxs-lookup"><span data-stu-id="80b5d-142">ITfDocumentMgr::GetTop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[<span data-ttu-id="80b5d-143">Итфранже:: SetText</span><span class="sxs-lookup"><span data-stu-id="80b5d-143">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="80b5d-144">Блокировки документов</span><span class="sxs-lookup"><span data-stu-id="80b5d-144">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="80b5d-145">Сеансы изменения</span><span class="sxs-lookup"><span data-stu-id="80b5d-145">Edit Sessions</span></span>](edit-sessions.md)
</dt> <dt>

[<span data-ttu-id="80b5d-146">ITfContext:: выделять</span><span class="sxs-lookup"><span data-stu-id="80b5d-146">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="80b5d-147">ITextStoreACP:: выделять</span><span class="sxs-lookup"><span data-stu-id="80b5d-147">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="80b5d-148">Итекстстореанчор:: выделять</span><span class="sxs-lookup"><span data-stu-id="80b5d-148">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




