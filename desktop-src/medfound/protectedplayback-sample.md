---
description: Показывает, как воспроизвести защищенное содержимое мультимедиа в Microsoft Media Foundation.
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: Пример Протектедплайбакк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee64b2a64ce4d40b6f15c2e5afb3b9a39e84c619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811578"
---
# <a name="protectedplayback-sample"></a><span data-ttu-id="800b6-103">Пример Протектедплайбакк</span><span class="sxs-lookup"><span data-stu-id="800b6-103">ProtectedPlayback Sample</span></span>

<span data-ttu-id="800b6-104">Показывает, как воспроизвести защищенное содержимое мультимедиа в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="800b6-104">Shows how to play protected media content in Microsoft Media Foundation.</span></span>

## <a name="usage"></a><span data-ttu-id="800b6-105">Использование</span><span class="sxs-lookup"><span data-stu-id="800b6-105">Usage</span></span>

<span data-ttu-id="800b6-106">Пример Протектедплайбакк создает приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="800b6-106">The ProtectedPlayback sample builds a Windows application.</span></span>

<span data-ttu-id="800b6-107">Чтобы воспроизвести локальный файл мультимедиа, выберите в меню **файл** пункт **Открыть файл** .</span><span class="sxs-lookup"><span data-stu-id="800b6-107">To play a local media file, select **Open File** from the **File** menu.</span></span> <span data-ttu-id="800b6-108">Чтобы указать файл по URL-адресу, выберите **Открыть URL-адрес** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="800b6-108">To specify a file by URL, select **Open URL** from the **File** menu.</span></span> <span data-ttu-id="800b6-109">После выбора файла воспроизведение начнется автоматически.</span><span class="sxs-lookup"><span data-stu-id="800b6-109">After you select a file, playback begins automatically.</span></span> <span data-ttu-id="800b6-110">Чтобы приостановить воспроизведение, нажмите клавишу пробел.</span><span class="sxs-lookup"><span data-stu-id="800b6-110">To pause playback, press the SPACEBAR.</span></span> <span data-ttu-id="800b6-111">Чтобы возобновить воспроизведение, снова нажмите клавишу пробел.</span><span class="sxs-lookup"><span data-stu-id="800b6-111">To resume playback, press the SPACEBAR again.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="800b6-112">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="800b6-112">APIs Demonstrated</span></span>

<span data-ttu-id="800b6-113">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="800b6-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="800b6-114">**имфконтентенаблер**</span><span class="sxs-lookup"><span data-stu-id="800b6-114">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [<span data-ttu-id="800b6-115">**имфконтентпротектионманажер**</span><span class="sxs-lookup"><span data-stu-id="800b6-115">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a><span data-ttu-id="800b6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="800b6-116">Requirements</span></span>



| <span data-ttu-id="800b6-117">Продукт</span><span class="sxs-lookup"><span data-stu-id="800b6-117">Product</span></span>                                                        | <span data-ttu-id="800b6-118">Version</span><span class="sxs-lookup"><span data-stu-id="800b6-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="800b6-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="800b6-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="800b6-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="800b6-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="800b6-121">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="800b6-121">Downloading the Sample</span></span>

<span data-ttu-id="800b6-122">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span><span class="sxs-lookup"><span data-stu-id="800b6-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="800b6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="800b6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="800b6-124">Воспроизведение защищенных файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="800b6-124">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="800b6-125">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="800b6-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

<span data-ttu-id="800b6-126">[Пример Мфплайер](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="800b6-126">[MFPlayer Sample](/previous-versions//bb970516(v=vs.85))</span></span>
</dt> </dl>

 

 
