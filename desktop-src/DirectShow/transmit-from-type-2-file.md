---
description: Передача из файла типа 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Передача из файла типа 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d1d6dec7c68cba177923dea04205d8dbc26faa8ff98cf5d6e79659fced46fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315723"
---
# <a name="transmit-from-type-2-file"></a>Передача из файла типа 2

Чтобы передать файл типа 2 при предварительном просмотре, используйте граф фильтра, показанный на следующей схеме.

![Тип-2. Передача с предварительной версией](images/dv2-transmit.png)

Файл типа 2 имеет два потока: один аудиопоток и один поток видео в кодировке DV. В этой диаграмме для объединения аудио и видеопотоков используется фильтр [DV мультиплексор](dv-muxer-filter.md) . Он отправляет поток с чередованием в фильтр МСДВ, но снова разделяет поток для предварительного просмотра.

Выполните сборку этого графа следующим образом:


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



Этот код выполняет несколько вызовов **RenderStream**:

Первые два способа соединяют фильтр источника с разделителем AVI и разделителем AVI с видеомультиплексором. в первом вызове построитель Graph захвата автоматически добавляет разделитель avi в граф и подключает один из выходных контактов разделителя avi к шлейфу DV. во втором вызове построитель Graph записи находит второй выходной пин-код разделителя AVI и подключается к мультиплексору DV.

Третий вызов **RenderStream** подключает DV мультиплексор к фильтру Tee с бесконечным ПИН-кодом. Следующий вызов соединяет один поток от бесконечного ПИН-кода Tee с фильтром записи МСДВ. Этот поток передается на устройство. Последний вызов **RenderStream** создает раздел предварительного просмотра диаграммы.

Если вы не хотите выполнять предварительный просмотр во время передачи, можно опустить неограниченный ПИН-код tee и просто подключить цифровой мультиплексор к фильтру МСДВ:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



