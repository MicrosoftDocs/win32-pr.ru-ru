---
description: Индексатор ASF — это компонент уровня Вмконтаинер, который используется для чтения или записи объектов индекса в файле ASF. В этом разделе содержатся сведения об использовании индексатора ASF для поиска в файле ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Использование индексатора для поиска в файле ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c674aa809c858856abf0c0e84c5d854b399c6fbc125ac9210e19b695380bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887244"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Использование индексатора для поиска в файле ASF

*ИНДЕКСАТОР* ASF — это компонент уровня вмконтаинер, который используется для чтения или записи объектов индекса в файле ASF. В этом разделе содержатся сведения об использовании индексатора ASF для поиска в файле ASF.

-   [Инициализация индексатора для поиска](#initializing-the-indexer-for-seeking)
-   [Получение расположения поиска.](#getting-the-seek-position)
-   [Связанные темы](#related-topics)

Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).

## <a name="initializing-the-indexer-for-seeking"></a>Инициализация индексатора для поиска

Чтобы инициализировать индексатор ASF для поиска, сделайте следующее:

1.  Вызовите [**мфкреатеасфиндексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) , чтобы создать новый экземпляр индексатора ASF.
2.  Вызовите метод [**имфасфиндексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) для инициализации индексатора. Этот метод получает сведения из заголовка ASF, чтобы определить, какие потоки ASF индексируются. По умолчанию объект индексатора настроен для поиска.
3.  Вызовите метод [**имфасфиндексер:: жетиндекспоситион**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) , чтобы найти смещение индекса в файле ASF.
4.  Вызовите функцию [**мфкреатеасфиндексербитестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) , чтобы создать байтовый поток для чтения индекса. Входные данные функции являются указателем на байтовый поток, который содержит ASF-файл, и смещение индекса (из предыдущего шага).
5.  Вызовите метод [**имфасфиндексер:: сетиндексбитестреамс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) , чтобы задать поток байтов индекса в индексаторе.

Следующий код показывает эти действия.


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a>Получение расположения поиска.

1.  Чтобы определить, индексируется ли определенный поток, вызовите метод [**имфасфиндексер:: жетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus). Если поток индексируется, параметр *пфисиндексед* получает значение **true**; в противном случае он получает значение **false**.
2.  По умолчанию индексатор использует поиск вперед. Для поиска в обратном порядке (т. е. поиска с конца файла) вызовите метод [**имфасфиндексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) и установите флаг **мфасф \_ \_ Read \_ для \_ реверсеплайбакк** . В противном случае пропустите этот шаг.
3.  Если поток индексируется, получите положение поиска для указанного времени презентации, вызвав [**имфасфиндексер:: жетсикпоситионфорвалуе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue). Этот метод считывает индекс ASF и находит запись индекса, ближайшую к запрошенному времени. Метод возвращает смещение в байтах для пакета данных, указанного в записи индекса. Смещение в байтах задается относительно начала объекта данных ASF.

Метод [**жетсикпоситионфорвалуе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) принимает указатель на структуру [**идентификатора ASF- \_ индекса \_**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) . Эта структура задает тип индекса и идентификатор потока. В настоящее время индекс должен иметь тип GUID \_ null, который указывает индексирование на основе времени.

Следующий код получает положение поиска по заданному идентификатору потока и целевому времени презентации. Если вызов завершается, он возвращает смещение данных в параметре *пкбдатаоффсет* и приблизительное фактическое время поиска в *фнсаппрокссиктиме*.


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Индексатор ASF](asf-index-object.md)
</dt> </dl>

 

 



