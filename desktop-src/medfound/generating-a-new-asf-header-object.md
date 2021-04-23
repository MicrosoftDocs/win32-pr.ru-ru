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
# <a name="generating-a-new-asf-header-object"></a><span data-ttu-id="8ad28-103">Создание нового объекта заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="8ad28-103">Generating a New ASF Header Object</span></span>

<span data-ttu-id="8ad28-104">Чтобы преобразовать сведения, содержащиеся в объекте Контентинфо, в формат объекта заголовка ASF, приложение должно вызвать [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="8ad28-104">To convert the information contained in the ContentInfo object to a binary ASF Header Object format, the application must call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="8ad28-105">Этот вызов должен быть сделан после создания пакетов данных, а объект Контентинфо содержит обновленную информацию.</span><span class="sxs-lookup"><span data-stu-id="8ad28-105">This call must be made after the data packets are generated and the ContentInfo object contains updated information.</span></span> <span data-ttu-id="8ad28-106">**Женератехеадер** возвращает указатель на буфер мультимедиа, содержащий сведения о заголовке в допустимом формате.</span><span class="sxs-lookup"><span data-stu-id="8ad28-106">**GenerateHeader** returns a pointer to a media buffer that contains the header information in the valid format.</span></span> <span data-ttu-id="8ad28-107">Затем приложение может записать данные, на которые указывает буфер мультимедиа, в начале нового ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="8ad28-107">The application can then write the data, pointed to by the media buffer, at the beginning of a new ASF file.</span></span>

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a><span data-ttu-id="8ad28-108">Запись нового объекта заголовка с помощью объекта Контентинфо</span><span class="sxs-lookup"><span data-stu-id="8ad28-108">To write a new Header Object by using the ContentInfo object</span></span>

1.  <span data-ttu-id="8ad28-109">Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать пустой объект контентинфо.</span><span class="sxs-lookup"><span data-stu-id="8ad28-109">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="8ad28-110">Вызовите [**имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , чтобы передать объект профиля объекту контентинфо.</span><span class="sxs-lookup"><span data-stu-id="8ad28-110">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to supply the profile object to the ContentInfo object.</span></span> <span data-ttu-id="8ad28-111">Дополнительные сведения о создании профилей см. [в разделе Создание профиля ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="8ad28-111">For information about creating profiles, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
3.  <span data-ttu-id="8ad28-112">Вызовите метод [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) и передайте **значение NULL** в параметр *пихеадер* и получите размер заполненного объекта контентинфо в параметре *пкбхеадер* .</span><span class="sxs-lookup"><span data-stu-id="8ad28-112">Call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) and pass **NULL** in the *pIHeader* parameter and receive the size of the populated ContentInfo object in the *pcbHeader* parameter.</span></span> <span data-ttu-id="8ad28-113">Приложение может использовать это значение для выделения памяти или буфера мультимедиа, который будет содержать объект заголовка.</span><span class="sxs-lookup"><span data-stu-id="8ad28-113">The application can use this value to allocate memory or the media buffer that will contain the Header Object.</span></span>

    <span data-ttu-id="8ad28-114">Полученный размер заголовка включает размер заполнения, который корректируется в зависимости от фактического размера объектов заголовка.</span><span class="sxs-lookup"><span data-stu-id="8ad28-114">The header size received includes the padding size, which is adjusted depending on the actual size of the header objects.</span></span> <span data-ttu-id="8ad28-115">Максимальный размер объектов заголовков составляет 10 МБ.</span><span class="sxs-lookup"><span data-stu-id="8ad28-115">The maximum size of the header objects is 10 MB.</span></span> <span data-ttu-id="8ad28-116">Если размер превышает это значение, **женератехеадер** завершается с ошибкой MF \_ E \_ ASF \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8ad28-116">If the size exceeds this value, **GenerateHeader** fails with the MF\_E\_ASF\_INVALIDDATA error.</span></span>

4.  <span data-ttu-id="8ad28-117">Вызовите [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) , чтобы создать буфер мультимедиа полученного размера на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="8ad28-117">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer of the received size in step 3.</span></span>
5.  <span data-ttu-id="8ad28-118">Вызовите **женератехеадер** еще раз, чтобы создать новый объект заголовка ASF из объекта контентинфо в буфере мультимедиа, созданном на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="8ad28-118">Call **GenerateHeader** again to generate the new ASF Header Object from the ContentInfo object in the media buffer created in step 4.</span></span>

    <span data-ttu-id="8ad28-119">Длина данных в буфере мультимедиа обновляется, а новый размер возвращается в параметре *пкбхеадер* .</span><span class="sxs-lookup"><span data-stu-id="8ad28-119">The length of the data in the media buffer is updated and the new size is returned in the *pcbHeader* parameter.</span></span>

6.  <span data-ttu-id="8ad28-120">Запишите содержимое буфера мультимедиа в начале файла.</span><span class="sxs-lookup"><span data-stu-id="8ad28-120">Write the contents of the media buffer at the beginning of the file.</span></span> <span data-ttu-id="8ad28-121">Приложение может использовать поток байтов для выполнения операции записи.</span><span class="sxs-lookup"><span data-stu-id="8ad28-121">The application can use the byte stream to perform the writing operation.</span></span> <span data-ttu-id="8ad28-122">Пример кода см. в разделе [**имфбитестреам:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="8ad28-122">For example code, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

### <a name="example"></a><span data-ttu-id="8ad28-123">Пример</span><span class="sxs-lookup"><span data-stu-id="8ad28-123">Example</span></span>

<span data-ttu-id="8ad28-124">В следующем примере кода показано, как создать объект Контентинфо и создать буфер мультимедиа для хранения нового объекта заголовка.</span><span class="sxs-lookup"><span data-stu-id="8ad28-124">The following example code shows how to create a ContentInfo object and generate a media buffer to store the new Header Object.</span></span> <span data-ttu-id="8ad28-125">Полный пример использования этого кода см. в разделе [учебник. копирование потоков ASF из одного файла в другой](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="8ad28-125">For a complete example that uses this code, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8ad28-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8ad28-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ad28-127">Запись объекта заголовка ASF для нового файла</span><span class="sxs-lookup"><span data-stu-id="8ad28-127">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



