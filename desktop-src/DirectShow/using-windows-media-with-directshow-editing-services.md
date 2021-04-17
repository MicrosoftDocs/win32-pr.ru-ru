---
description: Использование Windows Media с службами редактирования DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Использование Windows Media с службами редактирования DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674527"
---
# <a name="using-windows-media-with-directshow-editing-services"></a><span data-ttu-id="8a557-103">Использование Windows Media с службами редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a557-103">Using Windows Media With DirectShow Editing Services</span></span>

<span data-ttu-id="8a557-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="8a557-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8a557-105">В этом разделе описывается использование содержимого на основе Windows Media в приложении [служб редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="8a557-105">This section describes how to use Windows Media–based content in a [DirectShow Editing Services](directshow-editing-services.md) (DES) application.</span></span> <span data-ttu-id="8a557-106">Существует два основных сценария.</span><span class="sxs-lookup"><span data-stu-id="8a557-106">There are two main scenarios:</span></span>

-   <span data-ttu-id="8a557-107">Исходные клипы.</span><span class="sxs-lookup"><span data-stu-id="8a557-107">Source clips.</span></span> <span data-ttu-id="8a557-108">Проект DES может содержать аудио-и видеоклипы из файлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a557-108">A DES project can contain audio and video clips from Windows Media files.</span></span>
-   <span data-ttu-id="8a557-109">Конечный формат.</span><span class="sxs-lookup"><span data-stu-id="8a557-109">Target format.</span></span> <span data-ttu-id="8a557-110">Windows Media — идеальный формат для окончательных выходных данных проекта редактирования видео.</span><span class="sxs-lookup"><span data-stu-id="8a557-110">Windows Media is an ideal format for the final output of a video editing project.</span></span>

<span data-ttu-id="8a557-111">Для работы с файлами Windows Media приложение должно предоставить сертификат программного обеспечения, который также называется ключом.</span><span class="sxs-lookup"><span data-stu-id="8a557-111">To work with Windows Media files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="8a557-112">Для этого реализуется объект поставщика ключа.</span><span class="sxs-lookup"><span data-stu-id="8a557-112">It does this by implementing a key provider object.</span></span> <span data-ttu-id="8a557-113">Поставщик ключей — это COM-объект, предоставляющий интерфейс **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="8a557-113">The key provider is a COM object the exposes the **IServiceProvider** interface.</span></span> <span data-ttu-id="8a557-114">Сведения о реализации поставщика ключей см. в разделе [разблокировка пакета SDK Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="8a557-114">For information about implementing the key provider, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="8a557-115">Чтобы использовать DES с файлами Windows Media, для следующих объектов DES требуется программный ключ:</span><span class="sxs-lookup"><span data-stu-id="8a557-115">To use DES with Windows Media files, the following DES objects require the software key:</span></span>

-   <span data-ttu-id="8a557-116">Модуль подготовки отчетов для предварительного просмотра или записи файлов.</span><span class="sxs-lookup"><span data-stu-id="8a557-116">The render engine, for previewing or file writing.</span></span>
-   <span data-ttu-id="8a557-117">Объект Медиадет для получения видеокадров или типов мультимедиа из файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="8a557-117">The MediaDet object, to get video frames or media types from ASF files.</span></span>
-   <span data-ttu-id="8a557-118">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="8a557-118">\[!Important\]</span></span>  
    > <span data-ttu-id="8a557-119">Не используйте интеллектуальный модуль визуализации для чтения или записи файлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a557-119">Do not use the Smart Render Engine to read or write Windows Media files.</span></span> <span data-ttu-id="8a557-120">Всегда используйте базовый механизм визуализации (CLSID \_ рендеренгине).</span><span class="sxs-lookup"><span data-stu-id="8a557-120">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

     

<span data-ttu-id="8a557-121">Чтобы предоставить объекту программный ключ, запросите этот объект для интерфейса **IObjectWithSite** и вызовите **IObjectWithSite:: SetSite** с указателем на ваш поставщик ключей.</span><span class="sxs-lookup"><span data-stu-id="8a557-121">To give an object the software key, query that object for the **IObjectWithSite** interface and call **IObjectWithSite::SetSite** with a pointer to your key provider.</span></span> <span data-ttu-id="8a557-122">Например, следующий код предоставляет программный ключ модулю визуализации:</span><span class="sxs-lookup"><span data-stu-id="8a557-122">For example, the following code provides the software key to the render engine:</span></span>


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



<span data-ttu-id="8a557-123">Чтобы использовать клипы источника Windows Media в проекте DES, просто вызовите **IObjectWithSite:: SetSite** в подсистеме визуализации с указателем на ваш поставщик ключей.</span><span class="sxs-lookup"><span data-stu-id="8a557-123">To use Windows Media source clips in a DES project, simply call **IObjectWithSite::SetSite** on the render engine with a pointer to your key provider.</span></span>

<span data-ttu-id="8a557-124">Сведения о создании файлов Windows Media см. [в разделе запись файла Windows Media в Des](writing-a-windows-media-file-in-des.md).</span><span class="sxs-lookup"><span data-stu-id="8a557-124">For information about writing Windows Media files, see [Writing a Windows Media File in DES](writing-a-windows-media-file-in-des.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a557-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8a557-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a557-126">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a557-126">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



