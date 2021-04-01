---
title: Поддержка нескольких языков
description: Поддержка нескольких языков
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Пакет Windows Media Format SDK, поддерживающий несколько языков
- Пакет SDK для Windows Media Format, поддержка нескольких языков
- Windows Media Format SDK, языковая поддержка
- Расширенный формат систем (ASF), поддерживающий несколько языков
- ASF (Расширенный системный формат), поддержка нескольких языков
- Расширенный формат систем (ASF), поддержка нескольких языков
- ASF (Расширенный системный формат), поддержка нескольких языков
- Расширенный системный формат (ASF), поддержка языков
- ASF (Расширенный системный формат), поддержка языков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103987272"
---
# <a name="to-support-multiple-languages"></a>Поддержка нескольких языков

Можно поддерживать несколько языков в потоках и в метаданных. Основой поддержки нескольких языков в пакете SDK для Windows Media Format является интерфейс [**ивмлангуажелист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , который поддерживает список поддерживаемых языков. Список языков предоставляет каждому поддерживаемому языку индекс, который используется в различных объектах пакета SDK при работе с несколькими языками.

Метод [**ивмлангуажелист:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) добавляет язык в список. Вы можете узнать, какие языки уже находятся в списке, получая общее число языков с помощью [**ивмлангуажелист:: жетлангуажекаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) , а затем прокручивать языки, вызывающие [**Ивмлангуажелист:: жетлангуажедетаилс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) для каждого. Индекс языка отсчитывается от нуля.

## <a name="to-configure-mutual-exclusion-by-language"></a>Настройка взаимного исключения по языку

Настройка простого взаимоисключающего объекта по языку очень проста. Теперь каждый поток связан с языком. Язык, связанный с потоком, можно задать с помощью [**IWMStreamConfig3:: сетлангуаже**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage). После настройки всех взаимоисключающих потоков просто создайте объект взаимного исключения, как для любого другого типа. Затем вызовите [**ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) \_ , передав язык CLSID вммутекс \_ для типа.

Потоки, которые являются взаимоисключающими по языку, становятся более сложными, когда эксклюзивные потоки также взаимоисключающи по скорости потока. В этом случае необходимо использовать взаимоисключающие записи, выполнив следующие действия.

1.  Создайте объект взаимного исключения для потоков с разными скоростями разрядов на каждом языке. Дополнительные сведения о создании взаимоисключающего объекта по скорости потока см. в разделе Использование нескольких взаимоисключающих [исключений с несколькими битовыми частотами](using-multiple-bit-rate-mutual-exclusion.md).
2.  Создайте объект взаимного исключения. Вызовите [**ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) и передайте \_ язык CLSID вммутекс, \_ чтобы указать исключительные права по языку.
3.  Получите указатель на интерфейс [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) объекта взаимного исключения, созданного на шаге 2, вызвав метод **QueryInterface** [**ивммутуалексклусион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).
4.  Вызовите метод [**IWMMutualExclusion2:: аддрекорд**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) один раз для каждого языка, чтобы создать записи потока, которые будут взаимоисключающими.
5.  Для каждой записи, созданной на шаге 4, добавьте потоки соответствующего языка с вызовами метода [**IWMMutualExclusion2:: аддстреамфоррекорд**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Чтение файлов с несколькими языками

Объект "читатель" предоставляет методы для обнаружения доступных языков потоков в файле. Число поддерживаемых языков для выходных данных можно получить, вызвав [**IWMReaderAdvanced4:: жетлангуажекаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). Затем можно получить сведения о каждом языке с вызовами [**IWMReaderAdvanced4:: onlanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

Можно указать язык для воспроизведения, передав индекс этого языка в средство чтения с помощью вызова [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Это позволит выбрать указанный язык при сохранении автоматического выбора потоков для любых других взаимоисключающих объектов в файле.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Дополнительные разделы**](advanced-topics.md)
</dt> <dt>

[**Интерфейс Ивмлангуажелист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**Интерфейс Ивммутуалексклусион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Интерфейс IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**Интерфейс IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Интерфейс IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**Интерфейс IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




