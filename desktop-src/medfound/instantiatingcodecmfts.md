---
description: Создание экземпляра кодека МФТС
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Создание экземпляра кодека МФТС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263174"
---
# <a name="instantiating-codec-mfts"></a><span data-ttu-id="c0ce8-103">Создание экземпляра кодека МФТС</span><span class="sxs-lookup"><span data-stu-id="c0ce8-103">Instantiating Codec MFTs</span></span>

<span data-ttu-id="c0ce8-104">[Media Foundation преобразования](media-foundation-transforms.md) (МФТС) — это COM-объекты, реализующие интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="c0ce8-104">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) are COM objects that implement the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="c0ce8-105">MFT — это объект для преобразования мультимедийных данных в составе конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-105">An MFT is an object for transforming multimedia data as part of a pipeline.</span></span> <span data-ttu-id="c0ce8-106">Конвейер — это направленный ациклический граф, состоящий из источников мультимедиа, преобразований мультимедиа и приемников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-106">A pipeline is a directed acyclic graph, consisting of media sources, media transforms, and media sinks.</span></span> <span data-ttu-id="c0ce8-107">Конвейер обрабатывает потоковые данные мультимедиа в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-107">A pipeline processes streaming multimedia data asynchronously.</span></span>

<span data-ttu-id="c0ce8-108">Несмотря на то, что МФТС можно создавать и использовать независимо от Media Foundation инфраструктуры конвейера, предпочтительнее использовать платформу Медиафаундатион, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-108">Although MFTs can be instantiated and used independently of the Media Foundation pipeline infrastructure, it is preferable to use the MediaFoundation framework where possible.</span></span>

<span data-ttu-id="c0ce8-109">Можно создать MFT кодека, вызвав функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="c0ce8-109">You can create a codec MFT by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="c0ce8-110">Необходимо передать идентификатор класса MFT, идентификатор интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)и указатель на указатель **имфтрансформ** .</span><span class="sxs-lookup"><span data-stu-id="c0ce8-110">You must pass the class identifier of the MFT, the interface identifier of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), and a pointer to an **IMFTransform** pointer.</span></span>

<span data-ttu-id="c0ce8-111">Идентификаторы класса кодека МФТС определены как константы в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-111">The class identifiers of the codec MFTs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="c0ce8-112">Константа для идентификатора интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) — IID \_ имфтрансформ.</span><span class="sxs-lookup"><span data-stu-id="c0ce8-112">The constant for the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface identifier is IID\_IMFTransform.</span></span>

<span data-ttu-id="c0ce8-113">В следующем примере кода показано, как создать экземпляр MFT кодека:</span><span class="sxs-lookup"><span data-stu-id="c0ce8-113">The following code example demonstrates how to create an instance of a codec MFT:</span></span>


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a><span data-ttu-id="c0ce8-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c0ce8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0ce8-115">Работа с кодеками МФТС</span><span class="sxs-lookup"><span data-stu-id="c0ce8-115">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 
