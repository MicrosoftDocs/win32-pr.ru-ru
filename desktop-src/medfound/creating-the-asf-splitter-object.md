---
description: Создание объекта разделителя ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Создание объекта разделителя ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896581"
---
# <a name="creating-the-asf-splitter-object"></a><span data-ttu-id="2ca31-103">Создание объекта разделителя ASF</span><span class="sxs-lookup"><span data-stu-id="2ca31-103">Creating the ASF Splitter Object</span></span>

<span data-ttu-id="2ca31-104">Объект- *Разделитель* ASF — это объект слоя вмконтаинер, который анализирует объект данных ASF в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="2ca31-104">The ASF *splitter* object is a WMContainer layer object that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2ca31-105">Чтобы создать новый экземпляр объекта разделителя ASF, вызовите функцию [**мфкреатеасфсплиттер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="2ca31-105">To create a new instance of the ASF splitter object, call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function.</span></span> <span data-ttu-id="2ca31-106">Эта функция возвращает указатель на интерфейс [**имфасфсплиттер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) , представляющий пустой объект-разделитель.</span><span class="sxs-lookup"><span data-stu-id="2ca31-106">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface that represents an empty splitter object.</span></span>

<span data-ttu-id="2ca31-107">Прежде чем разделитель может начать анализ, приложение должно инициализировать разделитель данными из объекта заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="2ca31-107">Before the splitter can begin parsing, the application must initialize the splitter with information from the ASF Header Object.</span></span> <span data-ttu-id="2ca31-108">Чтобы инициализировать разделитель, вызовите метод [**имфасфсплиттер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="2ca31-108">To initialize the splitter, call the [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) method.</span></span> <span data-ttu-id="2ca31-109">Этот метод принимает указатель на [объект ASF контентинфо](asf-contentinfo-object.md) , который содержит сведения о заголовке ASF-файла для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="2ca31-109">This method takes a pointer to the [ASF ContentInfo Object](asf-contentinfo-object.md) that contains header information of the ASF file to parse.</span></span> <span data-ttu-id="2ca31-110">Приложение должно инициализировать объект Контентинфо перед передачей его в разделитель, чтобы характеристики файла мультимедиа были известны приложению.</span><span class="sxs-lookup"><span data-stu-id="2ca31-110">The application must initialize the ContentInfo object before passing it to the splitter so that the characteristics of the media file are known to the application.</span></span> <span data-ttu-id="2ca31-111">Метод **Initialize** разделителя извлекает сведения о потоке из объекта контентинфо, например номера потоков, поэтому разделитель может проанализировать пакеты данных.</span><span class="sxs-lookup"><span data-stu-id="2ca31-111">The splitter's **Initialize** method extracts stream information from the ContentInfo object, such as stream numbers, so the splitter can parse the data packets.</span></span>

### <a name="example"></a><span data-ttu-id="2ca31-112">Пример</span><span class="sxs-lookup"><span data-stu-id="2ca31-112">Example</span></span>

<span data-ttu-id="2ca31-113">В следующем примере кода показано, как создать разделитель и инициализировать его с помощью существующего объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="2ca31-113">The following code example shows how to create a splitter and initialize it with an existing ContentInfo object.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="2ca31-114">В этом примере функция [саферелеасе](saferelease.md) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2ca31-114">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2ca31-115">См. также</span><span class="sxs-lookup"><span data-stu-id="2ca31-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca31-116">Разделитель ASF</span><span class="sxs-lookup"><span data-stu-id="2ca31-116">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



