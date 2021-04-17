---
title: Выявление выходных номеров
description: Выявление выходных номеров
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK, идентифицирующие выходные номера
- Расширенный системный формат (ASF), идентифицирующие выходные номера
- ASF (Расширенный системный формат), определение выходных номеров
- Расширенный формат систем (ASF), выходные номера и форматы
- ASF (Расширенный системный формат), выходные номера и форматы
- выходные числа и форматы, определение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710233"
---
# <a name="to-identify-output-numbers"></a>Выявление выходных номеров

Чтобы узнать выходные номера загруженного файла, выполните следующие действия. Эти процедуры идентичны как для асинхронного чтения, так и для синхронного модуля чтения. Если имена интерфейсов различаются, методы синхронного чтения перечисляются в скобках после методов асинхронного модуля чтения.

1.  Создайте объект Reader и загрузите файл для чтения. Дополнительные сведения см. [в разделе Создание читателя и открытие файла](to-create-a-reader-and-open-a-file.md) (или [Создание синхронного средства чтения и открытие файла](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Получите общее число выходов для файла, вызвав [**ивмреадер:: жетаутпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (или [**Ивмсинкреадер:: жетаутпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).
3.  Перебрать выходные данные по одному за раз, выполнив следующие действия для каждого из них:
    -   Получите интерфейс [**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) для текущего вывода с помощью вызова [**Ивмреадер:: Жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (или [**ивмсинкреадер:: жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).
    -   Получите структуру [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для выходных данных, выполнив два вызова [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Выполните первый вызов, чтобы получить размер структуры, затем выделите память для нее и передайте указатель на выделенную память во втором вызове. Кроме того, можно вызвать метод [**ивммедиапропс:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), который доставляет основной тип, не требуя выделения памяти для **структуры \_ \_ типа мультимедиа WM** . Можно пропустить выходные данные неправильного основного типа.
    -   Получите основной тип носителя и подтип носителя из структуры **\_ \_ типа мультимедиа WM** . Эти значения хранятся в элементах данных **мажортипе** и **подтип** соответственно.
    -   Проверьте значение **WM \_ Media \_ Type. форматтипе**. Указывает тип структуры, содержащейся в буфере, на **WM \_ Media \_ Type. пбформат**. Дополнительные сведения о типах форматов см. в разделе [типы носителей](media-types.md).
    -   Выделите память для хранения структуры типа, указанного на предыдущем шаге. Скопируйте структуру в выделенную память. Для аудио и видео эта структура предоставляет необходимую информацию о том, как должны подготавливаться данные.

Синхронное средство чтения также предоставляет методы для получения связей между выходными числами и номерами потоков. Дополнительные сведения см. [в разделе Поиск номеров потоков и выходных номеров](to-find-stream-numbers-and-output-numbers.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Входы, потоки и выходные данные**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Интерфейс Ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Интерфейс Ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**Интерфейс Ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Работа с выходами**](working-with-outputs.md)
</dt> </dl>

 

 




