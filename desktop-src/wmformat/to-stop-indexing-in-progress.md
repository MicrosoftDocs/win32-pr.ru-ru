---
title: Завершение индексирования
description: Завершение индексирования
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Пакет SDK для формата мультимедиа, идет остановка индексирования
- Расширенный системный формат (ASF), остановка индексирования
- ASF (Расширенный системный формат), остановка индексирования
- индексы, остановка индексирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d441e42bc3c7033e776d353cf64fc5938183a4f8d720f086b4fb5fd9828be02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432627"
---
# <a name="to-stop-indexing-in-progress"></a>Завершение индексирования

После начала индексирования с помощью вызова [**ивминдексер:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing)индексатор обычно будет продолжать работу до индексирования файла. Можно остановить операции индексирования, вызвав метод [**ивминдексер:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) . После отмены индексирования можно снова вызвать **startIndex** , но индексатор будет начинаться с начала файла, а не возобновляться с момента отмены.

Поскольку **startIndex** является асинхронным вызовом, обычно требуется вызвать метод **Cancel** из другого потока или обработчика событий в приложении. как правило, **Cancel** вызывается из процедуры события, связанной с элементом управления "кнопка" Windows приложения.

При отмене индексирования индексатор передает сообщение о состоянии ВМТ \_ Closed, как будто файл был правильно проиндексирован.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивминдексер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




