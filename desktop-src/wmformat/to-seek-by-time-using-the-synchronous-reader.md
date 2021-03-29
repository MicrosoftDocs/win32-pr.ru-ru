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
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788809"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Поиск по времени с помощью синхронного модуля чтения

Чтобы найти данные с помощью синхронного модуля чтения, укажите диапазон для воспроизведения. Диапазон определяется начальным временем презентации и длительностью (в 100-наносекундных единицах).

Чтобы найти данные в файле ASF с помощью синхронного модуля чтения, выполните следующие действия.

1.  Укажите время и длительность выполнения образца доставки, вызвав [**ивмсинкреадер:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Этот метод не требует указания номера потока, так как время представления каждого потока должно быть уже синхронизировано.
2.  Начало извлечения образцов с вызовами метода [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Продолжайте работу, как обычно с синхронным модулем чтения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




