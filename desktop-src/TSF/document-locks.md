---
title: Блокировки документов
description: Блокировки документов
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Платформа текстовых служб (TSF), блокировки документов
- TSF (платформа текстовых служб), блокировки документов
- Приложения с поддержкой TSF, блокировки документов
- блокировки документов
- Платформа текстовых служб (TSF), размещение символов приложения (ACP)
- TSF (платформа текстовых служб), размещение символов приложения (ACP)
- Приложения с поддержкой TSF, размещение символов приложения (ACP)
- Позиции символов приложения (ACP)
- ACP (размещение символа приложения)
- Платформа текстовых служб (TSF), привязки
- TSF (платформа текстовых служб), привязки
- Приложения с поддержкой TSF, привязки
- Привязки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253027"
---
# <a name="document-locks"></a><span data-ttu-id="3c09e-116">Блокировки документов</span><span class="sxs-lookup"><span data-stu-id="3c09e-116">Document Locks</span></span>

## <a name="the-document-lock-protocol"></a><span data-ttu-id="3c09e-117">Протокол блокировки документов</span><span class="sxs-lookup"><span data-stu-id="3c09e-117">The Document Lock Protocol</span></span>

<span data-ttu-id="3c09e-118">Чтобы запросить блокировку документа для приложений на основе ACP, диспетчер TSF вызывает [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span><span class="sxs-lookup"><span data-stu-id="3c09e-118">To request a document lock for ACP-based applications, the TSF manager calls [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span></span> <span data-ttu-id="3c09e-119">Для приложений на основе привязки диспетчер TSF вызывает [итекстстореанчор:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span><span class="sxs-lookup"><span data-stu-id="3c09e-119">For anchor-based applications, the TSF manager calls [ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span></span> <span data-ttu-id="3c09e-120">Приложение предоставляет блокировку документа путем вызова [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (приложения на основе ACP) или [Итекстстореанчорсинк:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (приложения на основе привязки) внутри **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="3c09e-120">The application grants the document lock by calling [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-based applications) or [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (anchor-based applications) inside of **RequestLock**.</span></span> <span data-ttu-id="3c09e-121">Блокировка допустима только во время вызова **OnLockGranted** .</span><span class="sxs-lookup"><span data-stu-id="3c09e-121">The lock is only valid during the **OnLockGranted** call.</span></span> <span data-ttu-id="3c09e-122">Когда **OnLockGranted** возвращает, документ считается разблокированным.</span><span class="sxs-lookup"><span data-stu-id="3c09e-122">When **OnLockGranted** returns, the document is considered unlocked.</span></span>

## <a name="types-of-document-locks"></a><span data-ttu-id="3c09e-123">Типы блокировок документов</span><span class="sxs-lookup"><span data-stu-id="3c09e-123">Types of Document Locks</span></span>

<span data-ttu-id="3c09e-124">Существует два типа блокировок документов: только для чтения и для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3c09e-124">There are two types of document locks, read-only and read/write.</span></span> <span data-ttu-id="3c09e-125">Блокировка только для чтения позволяет менеджеру читать текст, но не может изменять или вставлять текст.</span><span class="sxs-lookup"><span data-stu-id="3c09e-125">A read-only lock enables the manager to read the text, but it cannot modify or insert text.</span></span> <span data-ttu-id="3c09e-126">Блокировка чтения и записи позволяет руководителю читать, изменять и вставлять текст.</span><span class="sxs-lookup"><span data-stu-id="3c09e-126">A read/write lock enables the manager to read, modify, and insert text.</span></span> <span data-ttu-id="3c09e-127">Запрашивается блокировка только для чтения путем указания TS \_ LF \_ Read в *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="3c09e-127">A read-only lock is requested by specifying TS\_LF\_READ in *dwFlags*.</span></span> <span data-ttu-id="3c09e-128">Запрос на блокировку чтения-записи запрашивается путем указания TS \_ LF \_ ReadWrite в *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="3c09e-128">A read/write lock is requested by specifying TS\_LF\_READWRITE in *dwFlags*.</span></span>

## <a name="asynchronous-and-synchronous-requests"></a><span data-ttu-id="3c09e-129">Асинхронные и синхронные запросы</span><span class="sxs-lookup"><span data-stu-id="3c09e-129">Asynchronous and Synchronous Requests</span></span>

<span data-ttu-id="3c09e-130">Запрос на блокировку может быть либо синхронным, либо асинхронным.</span><span class="sxs-lookup"><span data-stu-id="3c09e-130">A lock request can be either synchronous or asynchronous.</span></span> <span data-ttu-id="3c09e-131">Диспетчер запрашивает синхронную блокировку с помощью \_ \_ флага синхронизации TS LF в *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="3c09e-131">The manager requests a synchronous lock by using the TS\_LF\_SYNC flag in *dwFlags*.</span></span> <span data-ttu-id="3c09e-132">Если этот флаг отсутствует, запрос является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="3c09e-132">If this flag is not present, the request is asynchronous.</span></span>

## <a name="granting-the-lock"></a><span data-ttu-id="3c09e-133">Предоставление блокировки</span><span class="sxs-lookup"><span data-stu-id="3c09e-133">Granting the Lock</span></span>

<span data-ttu-id="3c09e-134">При вызове **RequestLock** приложение должно определить, заблокирован ли документ в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3c09e-134">When **RequestLock** is called, the application must determine if the document is currently locked.</span></span> <span data-ttu-id="3c09e-135">Если документ не заблокирован и нет других причин для запрета блокировки, приложение должно установить *параметре phrSession* в значение s \_ ОК и вернуть \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3c09e-135">If the document is not locked, and no other reason to deny the lock exists, the application should set *phrSession* to S\_OK and return S\_OK.</span></span>

<span data-ttu-id="3c09e-136">Если документ заблокирован, а запрос на блокировку является синхронным, приложение должно установить *параметре phrSession* в TS \_ E \_ синхронно и вернуть S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3c09e-136">If the document is locked and the lock request is synchronous, the application should set *phrSession* to TS\_E\_SYNCHRONOUS and return S\_OK.</span></span> <span data-ttu-id="3c09e-137">Это означает, что не удается предоставить синхронный запрос.</span><span class="sxs-lookup"><span data-stu-id="3c09e-137">This indicates that a synchronous request cannot be granted.</span></span>

<span data-ttu-id="3c09e-138">Если документ заблокирован и запрос на блокировку является асинхронным, приложение должно поставить запрос в очередь, установить *параметре phrSession* в TS \_ S \_ Async и вернуть s \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3c09e-138">If the document is locked and the lock request is asynchronous, the application should queue the request, set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="3c09e-139">Когда документ станет доступным, приложение должно удалить запрос из очереди и вызвать **OnLockGranted**.</span><span class="sxs-lookup"><span data-stu-id="3c09e-139">When the document becomes available, the application should remove the request from the queue and call **OnLockGranted**.</span></span> <span data-ttu-id="3c09e-140">Эта очередь запросов на блокировку необязательна; Существует один сценарий, который должен поддерживаться приложением.</span><span class="sxs-lookup"><span data-stu-id="3c09e-140">This queuing of lock requests is optional; there is one scenario that an application must support.</span></span> <span data-ttu-id="3c09e-141">Если документ имеет блокировку только для чтения, новый запрос на блокировку доступен для чтения и записи, а запрос является асинхронным, приложение вызывается в **OnLockGranted** , что вызвало повторный вызов **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="3c09e-141">If the document has a read-only lock, the new lock request is read/write and the request is asynchronous, the application has called into **OnLockGranted** , which has caused a reentrant call to **RequestLock**.</span></span> <span data-ttu-id="3c09e-142">Приложение должно установить *параметре phrSession* в TS \_ s \_ Async и вернуть s \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3c09e-142">The application should set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="3c09e-143">После того как вызов **OnLockGranted** возвращает, приложение должно обработать запрос на обновление, вызвав **OnLockGranted** еще раз с TS \_ LF \_ ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="3c09e-143">After the call to **OnLockGranted** returns, the application should process the upgrade request by calling **OnLockGranted** again with TS\_LF\_READWRITE.</span></span>

## <a name="lock-enforcement"></a><span data-ttu-id="3c09e-144">Принудительное применение блокировки</span><span class="sxs-lookup"><span data-stu-id="3c09e-144">Lock Enforcement</span></span>

<span data-ttu-id="3c09e-145">Перед предоставлением доступа к документу приложение должно убедиться, что существует соответствующий тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="3c09e-145">The application must ensure that the proper type of lock exists before allowing access to the document.</span></span> <span data-ttu-id="3c09e-146">Например, приложение должно убедиться, что документ имеет по крайней мере блокировку только для чтения, прежде чем разрешить продолжение [ITextStoreACP:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) или [Итекстстореанчор:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) .</span><span class="sxs-lookup"><span data-stu-id="3c09e-146">For example, the application should verify that a document has at least a read-only lock before allowing [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) to proceed.</span></span> <span data-ttu-id="3c09e-147">Если нужная блокировка не существует, приложение должно вернуть TF \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="3c09e-147">If the proper lock does not exist, the application should return TF\_E\_NOLOCK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c09e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="3c09e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c09e-149">Хранилища текста</span><span class="sxs-lookup"><span data-stu-id="3c09e-149">Text Stores</span></span>](text-stores.md)
</dt> <dt>

[<span data-ttu-id="3c09e-150">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="3c09e-150">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="3c09e-151">ITextStoreACPSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="3c09e-151">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="3c09e-152">ITextStoreACP:: GetText</span><span class="sxs-lookup"><span data-stu-id="3c09e-152">ITextStoreACP::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[<span data-ttu-id="3c09e-153">Итекстстореанчор:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="3c09e-153">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="3c09e-154">Итекстстореанчорсинк:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="3c09e-154">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="3c09e-155">Итекстстореанчор:: GetText</span><span class="sxs-lookup"><span data-stu-id="3c09e-155">ITextStoreAnchor::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




