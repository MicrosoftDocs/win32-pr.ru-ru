---
description: Работа с буферами мультимедиа
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Работа с буферами мультимедиа (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914163"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a><span data-ttu-id="c8a56-103">Работа с буферами мультимедиа (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="c8a56-103">Working with Media Buffers (Microsoft Media Foundation)</span></span>

<span data-ttu-id="c8a56-104">В этом разделе описывается использование интерфейса [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) для доступа к данным в буфере мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c8a56-104">This topic describes how to use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface to access the data in a media buffer.</span></span> <span data-ttu-id="c8a56-105">Все буферы мультимедиа предоставляют **имфмедиабуффер**, предназначенный для любого типа данных.</span><span class="sxs-lookup"><span data-stu-id="c8a56-105">All media buffers expose **IMFMediaBuffer**, which is designed for any type of data.</span></span> <span data-ttu-id="c8a56-106">Несжатые видеоматериалы — это особый случай, описанный в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="c8a56-106">Uncompressed video frames are a special case, described in the topic [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="buffer-size"></a><span data-ttu-id="c8a56-107">Размер буфера</span><span class="sxs-lookup"><span data-stu-id="c8a56-107">Buffer Size</span></span>

<span data-ttu-id="c8a56-108">С буфером мультимедиа связано два размера:</span><span class="sxs-lookup"><span data-stu-id="c8a56-108">A media buffer has two sizes associated with it:</span></span>

-   <span data-ttu-id="c8a56-109">*Максимальная длина* — это физический размер памяти, выделенной для буфера.</span><span class="sxs-lookup"><span data-stu-id="c8a56-109">The *maximum length* is the physical size of the memory that is allocated for the buffer.</span></span> <span data-ttu-id="c8a56-110">Это значение задается при создании буфера и не изменяется в течение времени существования буфера.</span><span class="sxs-lookup"><span data-stu-id="c8a56-110">This value is set when the buffer is created and does not change during the lifetime of the buffer.</span></span> <span data-ttu-id="c8a56-111">Максимальная длина указывает, сколько данных может храниться в буфере.</span><span class="sxs-lookup"><span data-stu-id="c8a56-111">The maximum length indicates how much data can be stored in the buffer.</span></span> <span data-ttu-id="c8a56-112">Чтобы найти максимальный размер, вызовите [**имфмедиабуффер:: @ MaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span><span class="sxs-lookup"><span data-stu-id="c8a56-112">To find the maximum size, call [**IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span></span>

-   <span data-ttu-id="c8a56-113">*Текущая длина* — это объем допустимых данных, которые в данный момент находятся в буфере.</span><span class="sxs-lookup"><span data-stu-id="c8a56-113">The *current length* is the amount of valid data that is currently in the buffer.</span></span> <span data-ttu-id="c8a56-114">При первом выделении буфера Текущая длина равна нулю, так как в буфере нет допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="c8a56-114">When the buffer is first allocated, the current length is zero, because there is no valid data in the buffer.</span></span> <span data-ttu-id="c8a56-115">При записи данных в буфер необходимо обновить текущую длину, вызвав [**имфмедиабуффер:: сеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span><span class="sxs-lookup"><span data-stu-id="c8a56-115">If you write any data to the buffer, you must update the current length by calling [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span></span> <span data-ttu-id="c8a56-116">Например, если в буфер записывается 100 байт данных, вызовите **сеткуррентленгс** со значением 100.</span><span class="sxs-lookup"><span data-stu-id="c8a56-116">For example, if you write 100 bytes of data into the buffer, call **SetCurrentLength** with the value 100.</span></span> <span data-ttu-id="c8a56-117">При чтении данных из буфера мультимедиа вызовите [**имфмедиабуффер:: жеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) , чтобы узнать, сколько данных в данный момент находится в буфере.</span><span class="sxs-lookup"><span data-stu-id="c8a56-117">If you read data from a media buffer, call [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) to find out how much data is currently in the buffer.</span></span> <span data-ttu-id="c8a56-118">Не читать после текущей длины.</span><span class="sxs-lookup"><span data-stu-id="c8a56-118">Do not read past the current length.</span></span> <span data-ttu-id="c8a56-119">Текущая длина не может превышать максимальную длину буфера.</span><span class="sxs-lookup"><span data-stu-id="c8a56-119">The current length can never exceed the maximum length of the buffer.</span></span>

## <a name="accessing-the-buffer-memory"></a><span data-ttu-id="c8a56-120">Доступ к буферной памяти</span><span class="sxs-lookup"><span data-stu-id="c8a56-120">Accessing the Buffer Memory</span></span>

<span data-ttu-id="c8a56-121">Чтобы получить доступ к памяти в буфере, вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="c8a56-121">To access the memory in the buffer, call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="c8a56-122">Этот метод возвращает указатель на начало блока памяти.</span><span class="sxs-lookup"><span data-stu-id="c8a56-122">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="c8a56-123">Он также возвращает максимальную длину и текущую длину.</span><span class="sxs-lookup"><span data-stu-id="c8a56-123">It also returns the maximum length and the current length.</span></span> <span data-ttu-id="c8a56-124">По завершении использования указателя вызовите [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="c8a56-124">When you are done using the pointer, call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="c8a56-125">Для записи данных в буфер мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="c8a56-125">To write data into a media buffer:</span></span>

1.  <span data-ttu-id="c8a56-126">Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , чтобы получить указатель на память.</span><span class="sxs-lookup"><span data-stu-id="c8a56-126">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="c8a56-127">Метод также возвращает максимальную длину буфера.</span><span class="sxs-lookup"><span data-stu-id="c8a56-127">The method also returns the buffer's maximum length.</span></span>
2.  <span data-ttu-id="c8a56-128">Запишите данные в память до максимальной длины буфера.</span><span class="sxs-lookup"><span data-stu-id="c8a56-128">Write your data into the memory, up to the buffer's maximum length.</span></span>
3.  <span data-ttu-id="c8a56-129">Вызовите [**имфмедиабуффер:: сеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) , чтобы обновить текущую длину.</span><span class="sxs-lookup"><span data-stu-id="c8a56-129">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the current length.</span></span> <span data-ttu-id="c8a56-130">Установите текущую длину, равную объему данных, записанных на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="c8a56-130">Set the current length equal to the amount of data that you wrote in step 2.</span></span>
4.  <span data-ttu-id="c8a56-131">Вызовите метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) , чтобы разблокировать буфер.</span><span class="sxs-lookup"><span data-stu-id="c8a56-131">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

<span data-ttu-id="c8a56-132">Чтение данных из буфера мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="c8a56-132">To read data from a media buffer:</span></span>

1.  <span data-ttu-id="c8a56-133">Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , чтобы получить указатель на память.</span><span class="sxs-lookup"><span data-stu-id="c8a56-133">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="c8a56-134">Метод также возвращает текущую длину буфера (объем допустимых данных в буфере).</span><span class="sxs-lookup"><span data-stu-id="c8a56-134">The method also returns the buffer's current length (the amount of valid data in the buffer).</span></span>
2.  <span data-ttu-id="c8a56-135">Считывает содержимое памяти до текущей длины.</span><span class="sxs-lookup"><span data-stu-id="c8a56-135">Read the contents of the memory, up to the current length.</span></span>
3.  <span data-ttu-id="c8a56-136">Вызовите метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) , чтобы разблокировать буфер.</span><span class="sxs-lookup"><span data-stu-id="c8a56-136">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

## <a name="creating-system-memory-buffers"></a><span data-ttu-id="c8a56-137">Создание буферов системной памяти</span><span class="sxs-lookup"><span data-stu-id="c8a56-137">Creating System Memory Buffers</span></span>

<span data-ttu-id="c8a56-138">Буфер системной памяти — это буфер мультимедиа, который управляет блоком системной памяти.</span><span class="sxs-lookup"><span data-stu-id="c8a56-138">The system memory buffer is a media buffer that manages a block of system memory.</span></span> <span data-ttu-id="c8a56-139">Чтобы создать экземпляр этого объекта, вызовите [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) или [**мфкреатеалигнедмеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) и укажите размер буфера.</span><span class="sxs-lookup"><span data-stu-id="c8a56-139">To create an instance of this object, call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) or [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) and specify a buffer size.</span></span> <span data-ttu-id="c8a56-140">Обе функции выделяют блок памяти и возвращают указатель [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="c8a56-140">Both functions allocate a block of memory and return an [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pointer.</span></span> <span data-ttu-id="c8a56-141">Память автоматически освобождается, когда счетчик ссылок буфера мультимедиа достигает нуля и объект уничтожается.</span><span class="sxs-lookup"><span data-stu-id="c8a56-141">The memory is automatically released when the media buffer's reference count reaches zero and the object is destroyed.</span></span>

<span data-ttu-id="c8a56-142">В следующем примере показано, как создать буфер системной памяти и выполнить запись в буфер.</span><span class="sxs-lookup"><span data-stu-id="c8a56-142">The following example shows how to create a system memory buffer and write to the buffer.</span></span>


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c8a56-143">См. также</span><span class="sxs-lookup"><span data-stu-id="c8a56-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a56-144">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c8a56-144">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="c8a56-145">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="c8a56-145">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



