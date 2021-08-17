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
ms.openlocfilehash: 89af01edd439dbac23e4dee4b5289101a9bd92ca8180b66b460096b797d32b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950924"
---
# <a name="text-stores"></a>Хранилища текста

## <a name="application-character-position-acp"></a>Позиции символов приложения (ACP)

ACP — это расположение символа или символов в текстовом потоке, выраженное в виде числа символов с начала потока текста. Поскольку модель ACP отсчитывается от нуля, первый символ в текстовом потоке имеет значение ACP, равное нулю. Например:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



В текстовом хранилище реализован объект, поддерживающий интерфейс [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , который позволяет выражать поток текста в ACP. Методы интерфейса **ITextStoreACP** используют диапазоны ACP текстового потока для изменения текста.

## <a name="anchor-based-applications"></a>Anchor-Based приложения

Для работы с текстом диспетчер использует собственные методы на основе ACP. Однако для клиентов [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) , поддерживающих [привязки](ranges.md), доступен подход на основе привязки, при котором диспетчер использует методы [итекстстореанчор](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) и [Итекстстореанчорсинк](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) для заключения в оболочку методов [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) и [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .

## <a name="document-access-control"></a>Управление доступом к документу

Хранилище текста управляет доступом к текстовому потоку с помощью [блокировок документов](document-locks.md). Для чтения или изменения хранилища текста диспетчер должен сначала установить приемник уведомлений, который поддерживает интерфейс [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) , вызвав метод [ITextStoreACP:: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) и передав указатель на приемник уведомлений. Приемник уведомлений позволяет диспетчеру получать блокировки документов в хранилище текста и получать уведомления при изменении хранилища текста не руководителем, например при вводе данных пользователем через приложение. Приемники уведомлений обсуждаются далее в этом разделе.

## <a name="how-to-initialize-the-text-store"></a>Инициализация хранилища текста

Приложение инициализирует хранилище текста, выполняя следующие действия.

1.  Создайте объект диспетчера потоков на основе интерфейса [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) , вызвав функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с указателем на объект диспетчера потоков. Ниже приведен пример кода реализации объекта диспетчера потоков.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Активируйте объект диспетчера потоков, вызвав метод [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) . Этот метод предоставляет указатель на [идентификатор клиента](tfclientid.md) , используемый для создания объекта контекста. Диспетчер потоков используется для реализации объекта диспетчера документов.
3.  Создайте объект диспетчера документов на основе интерфейса [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) , вызвав метод [ITfThreadMgr:: креатедокументмгр](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) с указателем на объект диспетчера документов. Объект диспетчера документов используется для реализации объекта контекста, который является хранилищем текста.
4.  Создайте объект контекста из диспетчера документов, вызвав метод [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) с указателем на объект хранилища текста и указателем на идентификатор клиента из активации диспетчера потоков. Ниже приведен пример создания объекта контекста.
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Отправьте объект контекста в стек с помощью метода [ITfDocumentMgr::P тельную](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) . Ниже приведен пример принудительной отправки объекта контекста в стек:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Изменение хранилища текста

Метод **ITfDocumentMgr::P тельную** вызывает **ITextStoreACP:: AdviseSink** с указателем на интерфейс приемника уведомлений для установки нового приемника уведомлений или изменения существующего приемника уведомлений. Приемник уведомлений получает уведомления, когда хранилище текста изменяется не руководителем, например входом пользователя в приложение. Приложения должны вызывать метод [итфсреадмгревентсинк:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) , когда входной метод получает фокус. Другие уведомления для диспетчера потоков предоставляются путем вызова соответствующих методов интерфейса **ITextStoreACPSink** .

Однако приложения не должны вызывать методы интерфейса **ITextStoreACPSink** в ответ на методы интерфейса **ITextStoreACP** . Приложения должны вызывать методы интерфейса **ITextStoreACPSink** , только если хранилище текста отличается от руководителя.

Содержимое хранилища текста можно изменить с помощью временного входного состояния, называемого [композицией](compositions.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Привязки](ranges.md)
</dt> <dt>

[Композиции](compositions.md)
</dt> <dt>

[Блокировки документов](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[итекстстореанчор](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[итекстстореанчорсинк](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[Итфсреадмгревентсинк:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[тфклиентид](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 