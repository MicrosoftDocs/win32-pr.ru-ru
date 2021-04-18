---
description: '\_Пример АУДИОДЕЛАЙ MFT'
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Пример MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656559"
---
# <a name="mft_audiodelay-sample"></a><span data-ttu-id="f46ec-103">\_Пример АУДИОДЕЛАЙ MFT</span><span class="sxs-lookup"><span data-stu-id="f46ec-103">MFT\_AudioDelay Sample</span></span>

<span data-ttu-id="f46ec-104">Показывает, как реализовать звуковой эффекты в виде Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="f46ec-104">Shows how to implement an audio effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="f46ec-105">Задержка аудио MFT принимает звук PCM в качестве входных данных, применяет результат задержки (echo) и выводит измененные аудиоданные.</span><span class="sxs-lookup"><span data-stu-id="f46ec-105">The audio delay MFT accepts PCM audio as input, applies a delay (echo) effect, and outputs the modified audio data.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="f46ec-106">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="f46ec-106">APIs Demonstrated</span></span>

<span data-ttu-id="f46ec-107">В этом образце демонстрируются следующие интерфейсы Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="f46ec-107">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="f46ec-108">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="f46ec-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="f46ec-109">Использование</span><span class="sxs-lookup"><span data-stu-id="f46ec-109">Usage</span></span>

<span data-ttu-id="f46ec-110">В \_ образце MFT аудиоделай создается библиотека DLL, которая является сервером COM для MFT.</span><span class="sxs-lookup"><span data-stu-id="f46ec-110">The MFT\_AudioDelay sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="f46ec-111">Перед использованием MFT необходимо зарегистрировать библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="f46ec-111">Before using the MFT, you must register the DLL.</span></span> <span data-ttu-id="f46ec-112">С помощью средства Топоедит можно создать топологию, включающую в себя временную запись MFT.</span><span class="sxs-lookup"><span data-stu-id="f46ec-112">You can use the TopoEdit tool to build a topology that includes the audio delay MFT.</span></span> <span data-ttu-id="f46ec-113">Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="f46ec-113">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span> <span data-ttu-id="f46ec-114">Можно также изменить [образец плайбаккфкс](/previous-versions//bb970336(v=vs.85)) для использования MFT.</span><span class="sxs-lookup"><span data-stu-id="f46ec-114">You can also modify the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)) to use the MFT.</span></span> <span data-ttu-id="f46ec-115">Вам потребуется изменить функцию Аддбранчтопартиалтопологи в проигрывателе Player. cpp.</span><span class="sxs-lookup"><span data-stu-id="f46ec-115">You will need to modify the AddBranchToPartialTopology function in Player.cpp.</span></span> <span data-ttu-id="f46ec-116">Измените следующую строку с:</span><span class="sxs-lookup"><span data-stu-id="f46ec-116">Change the following line from:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

<span data-ttu-id="f46ec-117">на:</span><span class="sxs-lookup"><span data-stu-id="f46ec-117">To:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

<span data-ttu-id="f46ec-118">Значение CLSID \_ делаймфт объявляется в файле заголовка аудиоделайууидс. h в \_ папке образца MFT аудиоделай.</span><span class="sxs-lookup"><span data-stu-id="f46ec-118">The value CLSID\_DelayMFT is declared in the header file AudioDelayUuids.h in the MFT\_AudioDelay sample folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="f46ec-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f46ec-119">Requirements</span></span>



| <span data-ttu-id="f46ec-120">Продукт</span><span class="sxs-lookup"><span data-stu-id="f46ec-120">Product</span></span>                                                        | <span data-ttu-id="f46ec-121">Version</span><span class="sxs-lookup"><span data-stu-id="f46ec-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="f46ec-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f46ec-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="f46ec-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f46ec-123">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f46ec-124">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="f46ec-124">Downloading the Sample</span></span>

<span data-ttu-id="f46ec-125">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span><span class="sxs-lookup"><span data-stu-id="f46ec-125">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f46ec-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f46ec-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f46ec-127">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f46ec-127">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="f46ec-128">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f46ec-128">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="f46ec-129">\_Пример использования градаций серого в MFT</span><span class="sxs-lookup"><span data-stu-id="f46ec-129">MFT\_Grayscale Sample</span></span>](mft-grayscale-sample.md)
</dt> <dt>

[<span data-ttu-id="f46ec-130">Запись пользовательского MFT</span><span class="sxs-lookup"><span data-stu-id="f46ec-130">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
