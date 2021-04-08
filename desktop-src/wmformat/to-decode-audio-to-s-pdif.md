---
title: Расшифровка аудио в S/PDIF
description: Расшифровка аудио в S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media Format SDK, декодирование аудио в S/PDIF
- Windows Media Format SDK, формат цифрового соединения Sony/Philips (S/PDIF)
- Расширенный системный формат (ASF), декодирование аудио в S/PDIF
- ASF (Расширенный системный формат), декодирование аудио в S/PDIF
- Формат ASF, Sony/Philips Digital Interconnect Format (S/PDIF)
- ASF (расширенный формат систем), формат цифровых соединений Sony/Philips (S/PDIF)
- Формат цифровых соединений Sony/Philips (S/PDIF), декодирование аудио
- S/PDIF (формат цифрового соединения Sony/Philips), декодирование аудио
- декодирование аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789223"
---
# <a name="to-decode-audio-to-spdif"></a>Расшифровка аудио в S/PDIF

Звук, закодированный с помощью кодека Windows Media Audio 9 Professional, можно декодировать в формат Digital Interconnect (S/PDIF) Sony/Philips. Чтобы создать выходные данные S/PDIF, выполните следующие действия.

1.  Откройте файл, содержащий поток Windows Media Audio 9 Professional, вызвав метод [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .
2.  Найдите выходной номер нужного потока. Дополнительные сведения см. [в разделе чтобы определить выходные номера](to-identify-output-numbers.md).
3.  Вызовите метод [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) , чтобы настроить выходные данные S/PDIF. Используйте g \_ всзенаблевмапроспдифаутпут для имени параметра. Тип данных — **ВМТ \_ типа \_ bool**; установите значение **true** , чтобы включить выходные данные S/PDIF.
4.  Получите интерфейс выходных свойств ([**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) требуемого формата выходных данных, вызвав метод [**Ивмреадер:: жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) . Дополнительные сведения о перечислении выходных форматов см. в разделе [назначение выходных форматов](assigning-output-formats.md).
5.  Задайте формат вывода, вызвав метод [**ивмреадер:: сетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) . Передайте указатель на интерфейс **ивмаутпутмедиапропс** , полученный на шаге 4.
6.  Внесите любые другие изменения в конфигурацию и начните воспроизведение.

> [!Note]  
> Вы можете выполнить описанные выше действия в синхронном модуле чтения, используя соответствующие методы интерфейса [**ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

 

В следующем примере кода показано, как настроить поток звука для вывода звука в виде данных S/PDIF. Эта функция предполагает, что файл уже загружен в модуль чтения и был идентифицирован выходной номер. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Дополнительные разделы**](advanced-topics.md)
</dt> <dt>

[**Чтение файлов ASF**](reading-asf-files.md)
</dt> <dt>

[**Интерфейс Ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Интерфейс IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




