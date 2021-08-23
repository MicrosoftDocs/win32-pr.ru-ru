---
description: В этом разделе показано, как написать индекс для ASF-файла.
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Использование индексатора для записи нового индекса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fbc604a9493f7feea61e34500e0f620a051b05b1431ec2d4917df9f8ed15b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034532"
---
# <a name="using-the-indexer-to-write-a-new-index"></a>Использование индексатора для записи нового индекса

В этом разделе показано, как написать индекс для ASF-файла.

Ниже приведена общая процедура создания индекса ASF.

1.  Инициализирует новый экземпляр объекта индексатора ASF, как описано в разделе [Создание и Настройка индексатора](indexer-creation-and-configuration.md).
2.  При необходимости настройте индексатор.
3.  Отправка пакетов данных ASF в индексатор.
4.  Зафиксируйте индекс.
5.  Получите завершенный индекс из индексатора и запишите его в поток.

## <a name="configure-the-indexer"></a>Настройка индексатора

Чтобы использовать индексатор для записи нового объекта индекса, в объекте индексатора должен быть установлен флаг МФАСФ, чтобы \_ индексатор \_ записывал \_ новый \_ набор индексов с вызовом [**имфасфиндексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) перед его инициализацией с помощью [**имфасфиндексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).

Если для создания индекса настроен индексатор, вызывающий объект выбирает потоки для индексирования. По умолчанию индексатор пытается создать объект индекса для всех потоков. По умолчанию интервал времени равен одной секунде.

[**Имфасфиндексер:: сетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) можно использовать для переопределения выбора потоков и типов индекса по умолчанию для объекта индексатора.

В следующем примере кода показана инициализация \_ \_ дескриптора и идентификатора ASF-индекса \_ \_ перед вызовом [**сетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



Для идентификатора индекса GUID должен быть задан тип GUID \_ null, чтобы указать, что для типа индекса будет использоваться время представления. Идентификатор индекса также должен быть инициализирован с помощью номера потока ASF Stream для индексирования. После задания идентификатора индекса используйте его для инициализации дескриптора индекса.

Структура дескриптора индекса содержит элементы, которые должны быть заданы перед вызовом [**сетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus). **Идентификатор** — это [**Структура \_ \_ идентификатора ASF-индекса**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) , которая определяет номер потока и тип индекса. **кперентрибитес** — число байтов, используемых для каждой записи индекса. Если значение МФАСФИНДЕКСЕР \_ в \_ \_ динамическом байте записи \_ , то элементы индекса имеют переменный размер. **двинтервал** — интервал индексирования. Значение МФАСФИНДЕКСЕР \_ без \_ фиксированного \_ интервала указывает на отсутствие фиксированного интервала индексирования.

## <a name="send-asf-data-packets-to-the-indexer"></a>Отправка пакетов данных ASF в индексатор

Поскольку индексатор является объектом уровня Вмконтаинер, он должен использоваться вместе с мультиплексором во время создания пакета.

Пакеты, возвращаемые из [**жетнекстпаккет**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) , могут быть отправлены в объект индексатора с помощью вызовов [**женератеиндексентриес**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) , где он создает записи индекса для каждого отправленного пакета.

В следующем коде показано, как это можно сделать:


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



Дополнительные сведения см. в разделе [Создание новых пакетов данных ASF](generating-new-asf-data-packets.md).

## <a name="commit-the-index"></a>Фиксация индекса

После того, как последний пакет создал запись индекса для него, индекс должен быть зафиксирован. Это делается с помощью вызова [**имфасфиндексер:: коммитиндекс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex). **Коммитиндекс** принимает указатель на объект контентинфо, описывающий содержимое ASF-файла. Фиксация индекса завершает индексирование и обновляет заголовок новыми сведениями о размере файла и возобновлении поиска.

## <a name="get-the-completed-index"></a>Получение завершенного индекса

Чтобы получить завершенный индекс из индексатора, выполните следующие действия.

1.  Вызовите [**имфасфиндексер:: жетиндексвритеспаце**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) , чтобы получить размер индекса.
2.  Вызовите [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) , чтобы создать буфер мультимедиа. Можно либо выделить буфер, достаточно большой для хранения всего индекса, чтобы выделить буфер меньшего размера и получить индекс в виде фрагментов.
3.  Вызовите метод [**имфасфиндексер:: жеткомплетединдекс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) , чтобы получить данные индекса. При первом вызове задайте для параметра *кбоффсетвисининдекс* значение 0. Если индекс получается в виде фрагментов, каждый раз увеличивается значение *кбоффсетвисининдекс* в размере данных из предыдущего вызова.
4.  Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , чтобы получить указатель на данные индекса и размер данных.
5.  Запишите данные индекса в файл ASF.
6.  Вызовите метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) , чтобы разблокировать буфер мультимедиа.
7.  Повторите шаги 3 – 6, пока не запишете весь индекс.

Следующий код показывает эти действия.


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Индексатор ASF](asf-index-object.md)
</dt> </dl>

 

 



