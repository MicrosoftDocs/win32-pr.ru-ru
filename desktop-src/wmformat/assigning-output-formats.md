---
title: Назначение форматов вывода
description: Назначение форматов вывода
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, назначение форматов выходных данных
- Расширенный системный формат (ASF), назначение форматов вывода
- ASF (Расширенный системный формат), назначение форматов вывода
- Расширенный формат систем (ASF), выходные номера и форматы
- ASF (Расширенный системный формат), выходные номера и форматы
- выходные числа и форматы, назначение
- кодеки, выходные номера и форматы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "105654269"
---
# <a name="assigning-output-formats"></a>Назначение форматов вывода

Некоторые кодеки могут распаковывать цифровые мультимедийные данные в несколько несжатых форматов. Вы можете найти все поддерживаемые форматы для определенного вывода, используя либо асинхронный читатель, либо синхронный модуль чтения.

Чтобы проверить все доступные форматы выходных данных, выполните следующие действия. Эти процедуры идентичны как для асинхронного чтения, так и для синхронного модуля чтения. Если имена интерфейсов различаются, методы синхронного чтения перечисляются в скобках после методов асинхронного модуля чтения.

1.  Создайте объект Reader и загрузите файл для чтения. Дополнительные сведения см. [в разделе Создание читателя и открытие файла](to-create-a-reader-and-open-a-file.md) (или [Создание синхронного средства чтения и открытие файла](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Определите выходные данные, для которых необходимо найти доступные форматы. Если вы не умеете знать, какие выходные данные вы хотите использовать, можно указать выходные данные в файле, используя процедуры в [для указания выходных номеров](to-identify-output-numbers.md).
3.  Получите общее число доступных форматов для требуемых выходных данных, вызвав [**ивмреадер:: жетаутпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (или [**Ивмсинкреадер:: жетаутпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).
4.  Выполните цикл по одному из доступных форматов, выполнив следующие действия для каждого из них:
    -   Получите интерфейс [**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) для текущего формата выходных данных, вызвав [**Ивмреадер:: Жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (или [**ивмсинкреадер:: жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).
    -   Получите структуру [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для выходного формата, выполнив два вызова [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Выполните первый вызов, чтобы получить размер структуры, затем выделите память для нее и передайте указатель на выделенную память во втором вызове.
    -   Найдите подтип носителя выходного формата в формате **WM \_ Media \_ Type.** подтип.
    -   Для видео, если текущий подтип является форматом, который вы хотите использовать для вывода, прервать цикл. В противном случае перейдите к следующей итерации.

        Для звука необходимо проверить значения в структуре **вавеформатекс** в соответствии с вашими требованиями. **WM \_ MEDIA \_ Type. пбформат** указывает на структуру **вавеформатекс** для звуковых выходов.

5.  После того как вы нашли нужные выходные данные, задайте их для использования с модулем чтения, вызвав [**ивмреадер:: сетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (или [**Ивмсинкреадер:: сетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)). Необходимо передать указатель на интерфейс **ивмаутпутмедиапропс** , полученный на первом шаге цикла.

## <a name="related-topics"></a>См. также

<dl> <dt>

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

 

 




