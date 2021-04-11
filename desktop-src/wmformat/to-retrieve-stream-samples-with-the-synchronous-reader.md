---
title: Получение примеров Stream с помощью синхронного модуля чтения
description: Получение примеров Stream с помощью синхронного модуля чтения
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Расширенный системный формат (ASF), получение примеров потоков
- ASF (Расширенный системный формат), получение примеров потоков
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- синхронные читатели, получение примеров потоков
- потоки, получение примеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133487"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a>Получение примеров Stream с помощью синхронного модуля чтения

Как и асинхронное средство чтения, синхронный читатель может получать выборки по номеру потока. В отличие от асинхронного модуля чтения, синхронный читатель может доставлять образцы потоков как сжатые, так и несжатые.

Чтобы получить примеры потоков, выполните следующие действия.

1.  В любой момент до или во время воспроизведения вызовите [**ивмсинкреадер:: сетреадстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) , передав нужный номер потока.
2.  Получите примеры с продолжающимися вызовами метода [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).

Вы можете проверить, выбран ли поток для выборки, вызвав [**ивмсинкреадер:: жетреадстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




