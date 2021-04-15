---
description: Создание нового объекта заголовка ASF
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Создание нового объекта заголовка ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539536"
---
# <a name="generating-a-new-asf-header-object"></a>Создание нового объекта заголовка ASF

Чтобы преобразовать сведения, содержащиеся в объекте Контентинфо, в формат объекта заголовка ASF, приложение должно вызвать [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Этот вызов должен быть сделан после создания пакетов данных, а объект Контентинфо содержит обновленную информацию. **Женератехеадер** возвращает указатель на буфер мультимедиа, содержащий сведения о заголовке в допустимом формате. Затем приложение может записать данные, на которые указывает буфер мультимедиа, в начале нового ASF-файла.

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>Запись нового объекта заголовка с помощью объекта Контентинфо

1.  Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать пустой объект контентинфо.
2.  Вызовите [**имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , чтобы передать объект профиля объекту контентинфо. Дополнительные сведения о создании профилей см. [в разделе Создание профиля ASF](creating-an-asf-profile.md).
3.  Вызовите метод [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) и передайте **значение NULL** в параметр *пихеадер* и получите размер заполненного объекта контентинфо в параметре *пкбхеадер* . Приложение может использовать это значение для выделения памяти или буфера мультимедиа, который будет содержать объект заголовка.

    Полученный размер заголовка включает размер заполнения, который корректируется в зависимости от фактического размера объектов заголовка. Максимальный размер объектов заголовков составляет 10 МБ. Если размер превышает это значение, **женератехеадер** завершается с ошибкой MF \_ E \_ ASF \_ INVALIDDATA.

4.  Вызовите [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) , чтобы создать буфер мультимедиа полученного размера на шаге 3.
5.  Вызовите **женератехеадер** еще раз, чтобы создать новый объект заголовка ASF из объекта контентинфо в буфере мультимедиа, созданном на шаге 4.

    Длина данных в буфере мультимедиа обновляется, а новый размер возвращается в параметре *пкбхеадер* .

6.  Запишите содержимое буфера мультимедиа в начале файла. Приложение может использовать поток байтов для выполнения операции записи. Пример кода см. в разделе [**имфбитестреам:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

### <a name="example"></a>Пример

В следующем примере кода показано, как создать объект Контентинфо и создать буфер мультимедиа для хранения нового объекта заголовка. Полный пример использования этого кода см. в разделе [учебник. копирование потоков ASF из одного файла в другой](tutorial--copying-asf-streams-from-one-file-to-another.md).


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись объекта заголовка ASF для нового файла](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



