---
description: Обработка данных в кодировщике
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Обработка данных в кодировщике
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711413"
---
# <a name="processing-data-in-the-encoder"></a>Обработка данных в кодировщике

После согласования типа входных данных и типа вывода для файла MFT кодировщика, как описано в разделе [согласование типов мультимедиа в кодировщике](media-type-negotiation-on-the-encoder.md), можно начать обработку образцов данных мультимедиа. Данные передаются в виде образцов мультимедиа (интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ), а также получаются из выходных данных в виде образцов мультимедиа.

Перед отправкой данных кодировщику для обработки необходимо выделить пример носителя и добавить один из нескольких буферов мультимедиа, содержащих данные мультимедиа, которые необходимо закодировать. Вызовите [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) и передайте указатель на выделенный пример носителя. Помимо примера носителя, для **ProcessInput** также требуется идентификатор входного потока. Чтобы получить идентификатор потока, вызовите метод [**имфтрансформ:: жетстреамидс**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids). Так как кодировщик предназначен только для одного и одного выходных данных, идентификаторы потоков всегда имеют значение 0.

Чтобы получить данные из кодировщика, вызовите [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Перед вызовом [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)необходимо выяснить, выделяет ли кодировщик образцы выходных данных, или необходимо сделать это явным образом. Для этого вызовите [**имфтрансформ:: жетаутпутстреаминфо**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo). Это возвращает образец выходных данных выходного носителя в структуре [**\_ \_ \_ сведений о потоке вывода MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Если кодировщик выделяет примеры носителей, он возвращает выходной поток MFT, \_ \_ \_ предоставляющий \_ флаг Samples в элементе **dwFlags** , а элемент **кбсизе** содержит ноль. Если кодировщику требуется выделить выходной буфер, создайте образец выходного носителя и связанный буфер мультимедиа на основе размера, возвращенного в **кбсизе**. При вызове [**процесссампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)передайте указатель на созданный образец носителя. Во время сеанса кодирования кодировщик заполняет буферы мультимедиа, на которые указывает образец выходного носителя, кодированными данными.

Чтобы начать сеанс кодирования, передайте пример входного носителя в кодировщик, вызвав метод [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). Кодировщик начинает обработку, а данные и создает один или несколько примеров выходных носителей, которые необходимо извлечь с помощью [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , если для \_ преобразования MF E \_ \_ требуется \_ больше \_ входных данных. При вызове метода **ProcessInput** для передачи большего числа входных данных, если имеются выходные данные для извлечения, то метод **ProcessInput** завершается с помощью MF \_ E \_ нотакцептинг. Кодировщик не принимает никаких входных данных, пока клиент не вызовет **ProcessOutput** по крайней мере один раз.

Необходимо задать точные метки времени и длительности для всех пройденных выборок. Метки времени не являются строго необходимыми, но помогают поддерживать синхронизацию аудио и видео. Если у вас нет меток времени для выборки, лучше оставить их, не используя неопределенные значения.

## <a name="encoder-processing-example"></a>Пример обработки кодировщика

В следующем примере кода показано, как вызвать [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , чтобы получить закодированный пример. Полный контекст этого примера см. в разделе [пример кода кодировщика](encoder-example-code.md).


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Мультиплексор ASF](asf-multiplexer.md)
</dt> <dt>

[Создание экземпляра MFT для кодировщика](instantiating-the-encoder-mft.md)
</dt> <dt>

[Кодировщики Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



