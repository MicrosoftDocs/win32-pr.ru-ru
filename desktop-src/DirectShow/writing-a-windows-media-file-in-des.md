---
description: Запись файла Windows Media в DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Запись файла Windows Media в DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684784"
---
# <a name="writing-a-windows-media-file-in-des"></a>Запись файла Windows Media в DES

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

В этом разделе описывается, как записать файл Windows Media с помощью [служб редактирования DirectShow](directshow-editing-services.md) (DES).

> [!IMPORTANT]
> Не используйте интеллектуальный модуль визуализации для записи файлов Windows Media. Всегда используйте базовый механизм визуализации (CLSID \_ рендеренгине).

 

Чтобы записать файл Windows Media, выполните следующие действия.

1.  Вызовите **SetSite** в подсистеме визуализации, указав указатель на поставщика ключа.
2.  Создание внешнего интерфейса графа. (См. раздел [Подготовка проекта к просмотру](rendering-a-project.md).)
3.  Создайте фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) и добавьте его в граф.
4.  Чтобы задать имя файла, используйте интерфейс [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) в фильтре модуля записи WM ASF.
5.  Настройка модуля записи WM ASF для использования профиля Windows Media. Каждый профиль имеет предопределенное количество потоков. Необходимо выбрать профиль, соответствующий группам в проекте.

    Интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) содержит несколько различных методов настройки профиля. Например, метод **конфигурефилтерусингпрофилегуид** указывает системный профиль в виде идентификатора GUID. Или можно использовать методы формата Windows Media для получения указателя **ивмпрофиле** , а затем вызвать [**Иконфигасфвритер:: конфигурефилтерусингпрофиле**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile). Дополнительные сведения см. [в разделе Настройка модуля записи ASF](configuring-the-asf-writer.md).

6.  Подключите внешний интерфейс к модулю записи ASF. Внешний интерфейс графа содержит один выходной ПИН-код для каждой группы. Если вы указали совместимый профиль, модуль записи ASF должен иметь соответствующий набор входных ПИН-кодов. Соедините каждый выходной закрепление с соответствующим входным закреплением. Проще всего это сделать с помощью метода [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . Сначала создайте новый экземпляр [построителя графа записи](capture-graph-builder.md) и инициализируйте его с помощью указателя на диспетчер графа фильтров:

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    Затем извлеките выходной ПИН-код для каждой группы, вызвав метод [**ирендеренгине:: жетграупаутпутпин**](irenderengine-getgroupoutputpin.md) . Вызовите **RenderStream** , чтобы подключить ПИН-код к модулю записи ASF:

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Windows Media с службами редактирования DirectShow](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



