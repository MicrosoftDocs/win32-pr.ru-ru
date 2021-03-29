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
# <a name="document-locks"></a>Блокировки документов

## <a name="the-document-lock-protocol"></a>Протокол блокировки документов

Чтобы запросить блокировку документа для приложений на основе ACP, диспетчер TSF вызывает [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock). Для приложений на основе привязки диспетчер TSF вызывает [итекстстореанчор:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock). Приложение предоставляет блокировку документа путем вызова [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (приложения на основе ACP) или [Итекстстореанчорсинк:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (приложения на основе привязки) внутри **RequestLock**. Блокировка допустима только во время вызова **OnLockGranted** . Когда **OnLockGranted** возвращает, документ считается разблокированным.

## <a name="types-of-document-locks"></a>Типы блокировок документов

Существует два типа блокировок документов: только для чтения и для чтения и записи. Блокировка только для чтения позволяет менеджеру читать текст, но не может изменять или вставлять текст. Блокировка чтения и записи позволяет руководителю читать, изменять и вставлять текст. Запрашивается блокировка только для чтения путем указания TS \_ LF \_ Read в *dwFlags*. Запрос на блокировку чтения-записи запрашивается путем указания TS \_ LF \_ ReadWrite в *dwFlags*.

## <a name="asynchronous-and-synchronous-requests"></a>Асинхронные и синхронные запросы

Запрос на блокировку может быть либо синхронным, либо асинхронным. Диспетчер запрашивает синхронную блокировку с помощью \_ \_ флага синхронизации TS LF в *dwFlags*. Если этот флаг отсутствует, запрос является асинхронным.

## <a name="granting-the-lock"></a>Предоставление блокировки

При вызове **RequestLock** приложение должно определить, заблокирован ли документ в данный момент. Если документ не заблокирован и нет других причин для запрета блокировки, приложение должно установить *параметре phrSession* в значение s \_ ОК и вернуть \_ ОК.

Если документ заблокирован, а запрос на блокировку является синхронным, приложение должно установить *параметре phrSession* в TS \_ E \_ синхронно и вернуть S \_ ОК. Это означает, что не удается предоставить синхронный запрос.

Если документ заблокирован и запрос на блокировку является асинхронным, приложение должно поставить запрос в очередь, установить *параметре phrSession* в TS \_ S \_ Async и вернуть s \_ ОК. Когда документ станет доступным, приложение должно удалить запрос из очереди и вызвать **OnLockGranted**. Эта очередь запросов на блокировку необязательна; Существует один сценарий, который должен поддерживаться приложением. Если документ имеет блокировку только для чтения, новый запрос на блокировку доступен для чтения и записи, а запрос является асинхронным, приложение вызывается в **OnLockGranted** , что вызвало повторный вызов **RequestLock**. Приложение должно установить *параметре phrSession* в TS \_ s \_ Async и вернуть s \_ ОК. После того как вызов **OnLockGranted** возвращает, приложение должно обработать запрос на обновление, вызвав **OnLockGranted** еще раз с TS \_ LF \_ ReadWrite.

## <a name="lock-enforcement"></a>Принудительное применение блокировки

Перед предоставлением доступа к документу приложение должно убедиться, что существует соответствующий тип блокировки. Например, приложение должно убедиться, что документ имеет по крайней мере блокировку только для чтения, прежде чем разрешить продолжение [ITextStoreACP:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) или [Итекстстореанчор:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) . Если нужная блокировка не существует, приложение должно вернуть TF \_ E \_ NOLOCK.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Хранилища текста](text-stores.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[Итекстстореанчор:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[Итекстстореанчорсинк:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[Итекстстореанчор:: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




