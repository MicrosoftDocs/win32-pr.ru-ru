---
title: Поиск по времени с помощью синхронного модуля чтения
description: Поиск по времени с помощью синхронного модуля чтения
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Расширенный формат систем (ASF), поиск по времени
- ASF (Расширенный системный формат), поиск по времени
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- синхронные читатели, поиск по времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74fb0cb4f73e70821347b82a9e5a2544eb9759e733fb164077b2fc007163db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432637"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Поиск по времени с помощью синхронного модуля чтения

Чтобы найти данные с помощью синхронного модуля чтения, укажите диапазон для воспроизведения. Диапазон определяется начальным временем презентации и длительностью (в 100-наносекундных единицах).

Чтобы найти данные в файле ASF с помощью синхронного модуля чтения, выполните следующие действия.

1.  Укажите время и длительность выполнения образца доставки, вызвав [**ивмсинкреадер:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Этот метод не требует указания номера потока, так как время представления каждого потока должно быть уже синхронизировано.
2.  Начало извлечения образцов с вызовами метода [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Продолжайте работу, как обычно с синхронным модулем чтения.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




