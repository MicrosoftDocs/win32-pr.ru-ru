---
title: Реализация обратного вызова OnSample
description: Реализация обратного вызова OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Расширенный системный формат (ASF), реализация обратного вызова OnStatus
- ASF (Расширенный системный формат), реализация обратного вызова OnStatus
- Расширенный формат систем (ASF), обратный вызов OnStatus
- ASF (Расширенный системный формат), обратный вызов OnStatus
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, реализация обратного вызова OnStatus
- Метод обратного вызова OnStatus, реализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00523ae28ec14feefb8249ff86a2b1600629c84cb245eb627b59b619a28a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027292"
---
# <a name="to-implement-the-onsample-callback"></a>Реализация обратного вызова OnSample

Асинхронный модуль чтения предоставляет образцы для управляющего приложения в порядке времени презентации, выполнив вызовы метода обратного вызова [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) . При создании приложения с помощью асинхронного модуля чтения необходимо реализовать **OnSample** , чтобы работать с несжатыми примерами. Обычно функции или методы, созданные для отрисовки содержимого, будут вызываться из **OnSample**.

Типичная реализация обратного вызова **OnSample** включает следующие шаги.

1.  Получите расположение и размер буфера, содержащего образец, вызвав [**инссбуффер:: жетбуфферандленгс**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) в буфере, переданном как *псампле*.
2.  Поветвление логики в зависимости от номера выхода. Выходной номер передается в **OnSample** как *дваутпутнумбер*.
3.  Включите логику отрисовки для каждого выходного номера, который требуется поддерживать. При отрисовке образцов из нескольких выходов может потребоваться синхронизация отрисовки.

Приложения, которые доставляют сжатые образцы из файлов ASF, должны реализовывать метод обратного вызова [**ивмреадеркаллбаккадванцед:: онстреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . Функции **онстреамсампле** практически идентичны, за исключением **того, что** он получает сжатые образцы по номеру потока вместо несжатых выборок по номеру выхода.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмреадеркаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**Интерфейс Ивмреадеркаллбаккадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Чтение файлов с помощью асинхронного модуля чтения**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Использование методов обратного вызова**](using-the-callback-methods.md)
</dt> </dl>

 

 




