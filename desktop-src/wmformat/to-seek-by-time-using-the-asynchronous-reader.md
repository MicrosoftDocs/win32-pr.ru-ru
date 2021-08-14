---
title: Поиск по времени с помощью асинхронного модуля чтения
description: Поиск по времени с помощью асинхронного модуля чтения
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Расширенный формат систем (ASF), поиск по времени
- ASF (Расширенный системный формат), поиск по времени
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, поиск по времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d480cade395cdbead99b1aedde8928c6fb18b4af15bf6b72c1bcc0dcd6dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196463"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Поиск по времени с помощью асинхронного модуля чтения

Если вы хотите найти определенное время презентации в файле ASF, необходимо правильно настроить файл. По умолчанию можно выполнять поиск по файлам только по звуку, но перед поиском необходимо проиндексировать видеофайлы. Если вы не знаете, как создать файл, можно проверить \_ атрибут g всзвмсикабле в заголовке файла, вызвав [**ивмхеадеринфо:: жетаттрибутебинаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Чтобы найти данные в файле ASF с помощью асинхронного модуля чтения, вызовите [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), передав требуемое время и длительность части файла, который требуется считать *кнсстарт* и *кнсдуратион* соответственно.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Чтение файлов с помощью асинхронного модуля чтения**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Считывание метаданных при воспроизведении**](reading-metadata-at-playback.md)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




