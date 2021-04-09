---
title: Хранилища текста
description: Хранилища текста
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Платформа текстовых служб (TSF), текстовые хранилища
- TSF (платформа текстовых служб), хранилища текста
- Приложения с поддержкой TSF, хранилища текста
- хранилища текста
- Платформа текстовых служб (TSF), размещение символов приложения (ACP)
- TSF (платформа текстовых служб), размещение символов приложения (ACP)
- Приложения с поддержкой TSF, размещение символов приложения (ACP)
- Позиции символов приложения (ACP)
- ACP (размещение символа приложения)
- Платформа текстовых служб (TSF), привязки
- TSF (платформа текстовых служб), привязки
- Приложения с поддержкой TSF, привязки
- Привязки
- Платформа текстовых служб (TSF), блокировки документов
- TSF (платформа текстовых служб), блокировки документов
- Приложения с поддержкой TSF, блокировки документов
- блокировки документов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070194"
---
# <a name="text-stores"></a><span data-ttu-id="4a606-120">Хранилища текста</span><span class="sxs-lookup"><span data-stu-id="4a606-120">Text Stores</span></span>

## <a name="application-character-position-acp"></a><span data-ttu-id="4a606-121">Позиции символов приложения (ACP)</span><span class="sxs-lookup"><span data-stu-id="4a606-121">Application Character Position (ACP)</span></span>

<span data-ttu-id="4a606-122">ACP — это расположение символа или символов в текстовом потоке, выраженное в виде числа символов с начала потока текста.</span><span class="sxs-lookup"><span data-stu-id="4a606-122">An ACP is the location of a character, or characters, in a text stream that is expressed as the number of characters from the start of the text stream.</span></span> <span data-ttu-id="4a606-123">Поскольку модель ACP отсчитывается от нуля, первый символ в текстовом потоке имеет значение ACP, равное нулю.</span><span class="sxs-lookup"><span data-stu-id="4a606-123">Because the ACP model is zero-based, the first character in a text stream has an ACP of zero.</span></span> <span data-ttu-id="4a606-124">Пример:</span><span class="sxs-lookup"><span data-stu-id="4a606-124">For example:</span></span>


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



<span data-ttu-id="4a606-125">В текстовом хранилище реализован объект, поддерживающий интерфейс [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , который позволяет выражать поток текста в ACP.</span><span class="sxs-lookup"><span data-stu-id="4a606-125">A text store implements an object that supports the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) interface, which enables the text stream to be expressed in an ACP.</span></span> <span data-ttu-id="4a606-126">Методы интерфейса **ITextStoreACP** используют диапазоны ACP текстового потока для изменения текста.</span><span class="sxs-lookup"><span data-stu-id="4a606-126">The **ITextStoreACP** interface methods use the ACP range of the text stream to modify the text.</span></span>

## <a name="anchor-based-applications"></a><span data-ttu-id="4a606-127">Anchor-Based приложения</span><span class="sxs-lookup"><span data-stu-id="4a606-127">Anchor-Based Applications</span></span>

<span data-ttu-id="4a606-128">Для работы с текстом диспетчер использует собственные методы на основе ACP.</span><span class="sxs-lookup"><span data-stu-id="4a606-128">The manager uses the ACP-based methods natively to manipulate text.</span></span> <span data-ttu-id="4a606-129">Однако для клиентов [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) , поддерживающих [привязки](ranges.md), доступен подход на основе привязки, при котором диспетчер использует методы [итекстстореанчор](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) и [Итекстстореанчорсинк](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) для заключения в оболочку методов [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) и [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .</span><span class="sxs-lookup"><span data-stu-id="4a606-129">However, an anchor-based approach is available for [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) clients that support [anchors](ranges.md), whereby the manager uses [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) and [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) methods to wrap the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) methods.</span></span>

## <a name="document-access-control"></a><span data-ttu-id="4a606-130">Управление доступом к документу</span><span class="sxs-lookup"><span data-stu-id="4a606-130">Document Access Control</span></span>

<span data-ttu-id="4a606-131">Хранилище текста управляет доступом к текстовому потоку с помощью [блокировок документов](document-locks.md).</span><span class="sxs-lookup"><span data-stu-id="4a606-131">The text store controls access to the text stream by using [document locks](document-locks.md).</span></span> <span data-ttu-id="4a606-132">Для чтения или изменения хранилища текста диспетчер должен сначала установить приемник уведомлений, который поддерживает интерфейс [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) , вызвав метод [ITextStoreACP:: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) и передав указатель на приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a606-132">To read or modify the text store, the manager must first install an advise sink that supports the [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) interface by calling the [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) method and passing a pointer to an advise sink.</span></span> <span data-ttu-id="4a606-133">Приемник уведомлений позволяет диспетчеру получать блокировки документов в хранилище текста и получать уведомления при изменении хранилища текста не руководителем, например при вводе данных пользователем через приложение.</span><span class="sxs-lookup"><span data-stu-id="4a606-133">The advise sink enables the manager to obtain a document locks on the text store and receive notifications when the text store is modified by something other than the manager, such as user input through the application.</span></span> <span data-ttu-id="4a606-134">Приемники уведомлений обсуждаются далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="4a606-134">Advise sinks are discussed later in this topic.</span></span>

## <a name="how-to-initialize-the-text-store"></a><span data-ttu-id="4a606-135">Инициализация хранилища текста</span><span class="sxs-lookup"><span data-stu-id="4a606-135">How To Initialize the Text Store</span></span>

<span data-ttu-id="4a606-136">Приложение инициализирует хранилище текста, выполняя следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4a606-136">An application initializes a text store by completing the following steps:</span></span>

1.  <span data-ttu-id="4a606-137">Создайте объект диспетчера потоков на основе интерфейса [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) , вызвав функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с указателем на объект диспетчера потоков.</span><span class="sxs-lookup"><span data-stu-id="4a606-137">Create a thread manager object based on the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function with a pointer to a thread manager object.</span></span> <span data-ttu-id="4a606-138">Ниже приведен пример кода реализации объекта диспетчера потоков.</span><span class="sxs-lookup"><span data-stu-id="4a606-138">The following is a code example of implementing a thread manager object.</span></span>
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  <span data-ttu-id="4a606-139">Активируйте объект диспетчера потоков, вызвав метод [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) .</span><span class="sxs-lookup"><span data-stu-id="4a606-139">Activate the thread manager object by calling the [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) method.</span></span> <span data-ttu-id="4a606-140">Этот метод предоставляет указатель на [идентификатор клиента](tfclientid.md) , используемый для создания объекта контекста.</span><span class="sxs-lookup"><span data-stu-id="4a606-140">This method supplies a pointer to a [client identifier](tfclientid.md) used to create a context object.</span></span> <span data-ttu-id="4a606-141">Диспетчер потоков используется для реализации объекта диспетчера документов.</span><span class="sxs-lookup"><span data-stu-id="4a606-141">The thread manager is used to implement a document manager object.</span></span>
3.  <span data-ttu-id="4a606-142">Создайте объект диспетчера документов на основе интерфейса [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) , вызвав метод [ITfThreadMgr:: креатедокументмгр](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) с указателем на объект диспетчера документов.</span><span class="sxs-lookup"><span data-stu-id="4a606-142">Create a document manager object based on the [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) interface by calling the [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) method with a pointer to the document manager object.</span></span> <span data-ttu-id="4a606-143">Объект диспетчера документов используется для реализации объекта контекста, который является хранилищем текста.</span><span class="sxs-lookup"><span data-stu-id="4a606-143">The document manager object is used to implement a context object that is the text store.</span></span>
4.  <span data-ttu-id="4a606-144">Создайте объект контекста из диспетчера документов, вызвав метод [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) с указателем на объект хранилища текста и указателем на идентификатор клиента из активации диспетчера потоков.</span><span class="sxs-lookup"><span data-stu-id="4a606-144">Create a context object from the document manager by calling the [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) method with the pointer to the text store object and a pointer to the client identifier from activating the thread manager.</span></span> <span data-ttu-id="4a606-145">Ниже приведен пример создания объекта контекста.</span><span class="sxs-lookup"><span data-stu-id="4a606-145">The following is an example of creating a context object:</span></span>
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  <span data-ttu-id="4a606-146">Отправьте объект контекста в стек с помощью метода [ITfDocumentMgr::P тельную](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) .</span><span class="sxs-lookup"><span data-stu-id="4a606-146">Push the context object onto the stack with the [ITfDocumentMgr::Push](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) method.</span></span> <span data-ttu-id="4a606-147">Ниже приведен пример принудительной отправки объекта контекста в стек:</span><span class="sxs-lookup"><span data-stu-id="4a606-147">The following is an example of pushing the context object onto the stack:</span></span>
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a><span data-ttu-id="4a606-148">Изменение хранилища текста</span><span class="sxs-lookup"><span data-stu-id="4a606-148">How To Modify the Text Store</span></span>

<span data-ttu-id="4a606-149">Метод **ITfDocumentMgr::P тельную** вызывает **ITextStoreACP:: AdviseSink** с указателем на интерфейс приемника уведомлений для установки нового приемника уведомлений или изменения существующего приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a606-149">The **ITfDocumentMgr::Push** method calls **ITextStoreACP::AdviseSink** with a pointer to the advise sink interface to install a new advise sink or modify an existing advise sink.</span></span> <span data-ttu-id="4a606-150">Приемник уведомлений получает уведомления, когда хранилище текста изменяется не руководителем, например входом пользователя в приложение.</span><span class="sxs-lookup"><span data-stu-id="4a606-150">The advise sink receives notifications when the text store is modified by something other than the manager, such as user input to the application.</span></span> <span data-ttu-id="4a606-151">Приложения должны вызывать метод [итфсреадмгревентсинк:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) , когда входной метод получает фокус.</span><span class="sxs-lookup"><span data-stu-id="4a606-151">Applications must call the [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) method when the input method obtains the focus.</span></span> <span data-ttu-id="4a606-152">Другие уведомления для диспетчера потоков предоставляются путем вызова соответствующих методов интерфейса **ITextStoreACPSink** .</span><span class="sxs-lookup"><span data-stu-id="4a606-152">Other notifications to the thread manager are provided by calling to the appropriate **ITextStoreACPSink** interface methods.</span></span>

<span data-ttu-id="4a606-153">Однако приложения не должны вызывать методы интерфейса **ITextStoreACPSink** в ответ на методы интерфейса **ITextStoreACP** .</span><span class="sxs-lookup"><span data-stu-id="4a606-153">However, applications should not call the **ITextStoreACPSink** interface methods in response to **ITextStoreACP** interface methods.</span></span> <span data-ttu-id="4a606-154">Приложения должны вызывать методы интерфейса **ITextStoreACPSink** , только если хранилище текста отличается от руководителя.</span><span class="sxs-lookup"><span data-stu-id="4a606-154">Applications should only call **ITextStoreACPSink** interface methods when the text store is modified by something other than the manager.</span></span>

<span data-ttu-id="4a606-155">Содержимое хранилища текста можно изменить с помощью временного входного состояния, называемого [композицией](compositions.md).</span><span class="sxs-lookup"><span data-stu-id="4a606-155">The contents of the text store can be modified with a temporary input state called a [composition](compositions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a606-156">См. также</span><span class="sxs-lookup"><span data-stu-id="4a606-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a606-157">Привязки</span><span class="sxs-lookup"><span data-stu-id="4a606-157">Anchors</span></span>](ranges.md)
</dt> <dt>

[<span data-ttu-id="4a606-158">Композиции</span><span class="sxs-lookup"><span data-stu-id="4a606-158">Compositions</span></span>](compositions.md)
</dt> <dt>

[<span data-ttu-id="4a606-159">Блокировки документов</span><span class="sxs-lookup"><span data-stu-id="4a606-159">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="4a606-160">ITextStoreACPSink</span><span class="sxs-lookup"><span data-stu-id="4a606-160">ITextStoreACPSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[<span data-ttu-id="4a606-161">ITextStoreACP</span><span class="sxs-lookup"><span data-stu-id="4a606-161">ITextStoreACP</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="4a606-162">итекстстореанчор</span><span class="sxs-lookup"><span data-stu-id="4a606-162">ITextStoreAnchor</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[<span data-ttu-id="4a606-163">итекстстореанчорсинк</span><span class="sxs-lookup"><span data-stu-id="4a606-163">ITextStoreAnchorSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[<span data-ttu-id="4a606-164">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="4a606-164">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="4a606-165">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="4a606-165">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="4a606-166">Итфсреадмгревентсинк:: OnSetFocus</span><span class="sxs-lookup"><span data-stu-id="4a606-166">ITfThreadMgrEventSink::OnSetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[<span data-ttu-id="4a606-167">тфклиентид</span><span class="sxs-lookup"><span data-stu-id="4a606-167">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="4a606-168">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="4a606-168">Microsoft Active Accessibility</span></span>](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 