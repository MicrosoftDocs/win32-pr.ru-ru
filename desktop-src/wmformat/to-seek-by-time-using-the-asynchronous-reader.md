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
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788814"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Поиск по времени с помощью асинхронного модуля чтения

Если вы хотите найти определенное время презентации в файле ASF, необходимо правильно настроить файл. По умолчанию можно выполнять поиск по файлам только по звуку, но перед поиском необходимо проиндексировать видеофайлы. Если вы не знаете, как создать файл, можно проверить \_ атрибут g всзвмсикабле в заголовке файла, вызвав [**ивмхеадеринфо:: жетаттрибутебинаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Чтобы найти данные в файле ASF с помощью асинхронного модуля чтения, вызовите [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), передав требуемое время и длительность части файла, который требуется считать *кнсстарт* и *кнсдуратион* соответственно.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Чтение файлов с помощью асинхронного модуля чтения**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Считывание метаданных при воспроизведении**](reading-metadata-at-playback.md)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




