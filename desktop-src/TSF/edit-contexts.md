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
# <a name="edit-contexts"></a>Изменение контекстов

## <a name="applications"></a>Приложения

Чтобы создать контекст редактирования, приложение вызывает [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).

## <a name="text-services"></a>Текстовые службы

В текстовой службе часто используется текущий активный контекст редактирования. Текущий активный контекст редактирования — это контекст редактирования в верхней части стека активного диспетчера документов. Чтобы получить текущий активный контекст, служба текстового ввода вызывает [ITfThreadMgr:: Focus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) для получения активного диспетчера документов, а затем вызывает [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) , чтобы получить контекст редактирования в верхней части стека.

В некоторых случаях для текстового сервиса требуется собственный контекст редактирования. Для создания контекста редактирования текстовая служба вызывает **ITfDocumentMgr:: CreateContext**.

## <a name="edit-cookies"></a>Изменить файлы cookie

Многие методы, такие как [итфранже:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), нуждаются в способе указать контекст редактирования, который имеет [блокировку документа](document-locks.md)только для чтения или чтения и записи. Блокировка документа достигается за счет согласования между диспетчером TSF и приложением. Служба текстового ввода не может выполнить это согласование напрямую. Служба текстового ввода может получить блокировку, запрашивая [сеанс редактирования](edit-sessions.md) с конкретным контекстом и доступом только для чтения или чтения и записи. При предоставлении сеанса редактирования текстовая служба получает *файл cookie редактирования* , который определяет контекст редактирования с запрошенным доступом. Затем этот файл cookie передается в метод для обнаружения контекста редактирования с правильным доступом.

**ITfDocumentMgr:: CreateContext** также предоставляет файл cookie редактирования для создателя контекста. Этот файл cookie имеет доступ только для чтения, и изменить уровень доступа невозможно. В действительности, диспетчер TSF не согласовывает блокировку документа для этого файла редактирования. Файл cookie внутренне помечен как "только для чтения", но документ фактически не блокируется. Например, если создатель контекста вызывает [ITfContext::-SELECT](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) с изменением cookie, возвращенным **ITfDocumentMgr:: CreateContext** , это приводит к вызову [ITextStoreACP::-SELECT](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) или [итекстстореанчор::-SELECT](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) . Перед получением выбора приложение определит, существует ли блокировка документа. Так как блокировка не существует, приложение завершится ошибкой с помощью TS \_ E \_ Lock. Это означает, что если приложение вызывает метод с этим файлом cookie, который приводит к вызову одного из методов хранилища текста приложения, он должен обработать этот случай, поскольку приложение на самом деле не будет блокировать документ.

Если автору контекста требуется изменить файл cookie с доступом на чтение и запись, он должен установить собственный сеанс редактирования.

## <a name="related-topics"></a>См. также

<dl> <dt>

[ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr:: Focus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[Итфранже:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Блокировки документов](document-locks.md)
</dt> <dt>

[Сеансы изменения](edit-sessions.md)
</dt> <dt>

[ITfContext:: выделять](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: выделять](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[Итекстстореанчор:: выделять](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




