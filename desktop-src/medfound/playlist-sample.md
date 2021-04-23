---
description: Пример списка воспроизведения
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Пример списка воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711415"
---
# <a name="playlist-sample"></a><span data-ttu-id="34896-103">Пример списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="34896-103">Playlist Sample</span></span>

<span data-ttu-id="34896-104">Показывает, как использовать Microsoft Media Foundation для воспроизведения последовательности звуковых файлов в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="34896-104">Shows how to use Microsoft Media Foundation to play a sequence of audio files in a playlist.</span></span> <span data-ttu-id="34896-105">В примере используется [источник Sequencer](sequencer-source.md) для создания списка воспроизведения и управления им.</span><span class="sxs-lookup"><span data-stu-id="34896-105">The sample uses the [Sequencer Source](sequencer-source.md) to create and manage the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="34896-106">Этот пример больше не включен в пакет SDK.</span><span class="sxs-lookup"><span data-stu-id="34896-106">This sample is no longer included in the SDK.</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="34896-107">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="34896-107">APIs Demonstrated</span></span>

<span data-ttu-id="34896-108">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="34896-108">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="34896-109">**имфмедиасаурцетопологипровидер**</span><span class="sxs-lookup"><span data-stu-id="34896-109">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [<span data-ttu-id="34896-110">**имфмедиасессион**</span><span class="sxs-lookup"><span data-stu-id="34896-110">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [<span data-ttu-id="34896-111">**имфсекуенцерсаурце**</span><span class="sxs-lookup"><span data-stu-id="34896-111">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a><span data-ttu-id="34896-112">Использование</span><span class="sxs-lookup"><span data-stu-id="34896-112">Usage</span></span>

<span data-ttu-id="34896-113">Пример списка воспроизведения создает приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="34896-113">The Playlist sample builds a Windows application.</span></span>

-   <span data-ttu-id="34896-114">Чтобы создать новый список воспроизведения, выберите в меню **файл** пункт **Добавить в список воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="34896-114">To create a new playlist, select **Add to Playlist** from the **File** menu.</span></span> <span data-ttu-id="34896-115">В диалоговом окне **открытия файла** выберите один или несколько звуковых файлов.</span><span class="sxs-lookup"><span data-stu-id="34896-115">In the **Open File** dialog, select one or more audio files.</span></span> <span data-ttu-id="34896-116">Файлы добавляются в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="34896-116">The files are added to the playlist.</span></span>
-   <span data-ttu-id="34896-117">Чтобы воспроизвести последовательность, нажмите кнопку **воспроизвести**.</span><span class="sxs-lookup"><span data-stu-id="34896-117">To play the sequence, click **Play**.</span></span>
-   <span data-ttu-id="34896-118">Чтобы приостановить текущий сегмент, нажмите кнопку **приостановить**.</span><span class="sxs-lookup"><span data-stu-id="34896-118">To pause the current segment, click **Pause**.</span></span>
-   <span data-ttu-id="34896-119">Чтобы прерывать текущий сегмент, нажмите кнопку " **Закрыть**".</span><span class="sxs-lookup"><span data-stu-id="34896-119">To stop the current segment, click **Stop**.</span></span>
-   <span data-ttu-id="34896-120">Чтобы перейти к файлу, дважды щелкните его в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="34896-120">To skip to a file, double-click the item in the playlist.</span></span>
-   <span data-ttu-id="34896-121">Чтобы удалить файл из списка воспроизведения, выберите его в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="34896-121">To delete a file from the playlist, select the item in the playlist.</span></span> <span data-ttu-id="34896-122">Затем в меню **файл** выберите команду **удалить из списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="34896-122">Then select **Remove from Playlist** from the **File** menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="34896-123">Требования</span><span class="sxs-lookup"><span data-stu-id="34896-123">Requirements</span></span>



| <span data-ttu-id="34896-124">Продукт</span><span class="sxs-lookup"><span data-stu-id="34896-124">Product</span></span>                                                        | <span data-ttu-id="34896-125">Version</span><span class="sxs-lookup"><span data-stu-id="34896-125">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="34896-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="34896-126">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="34896-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="34896-127">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="34896-128">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="34896-128">Downloading the Sample</span></span>

<span data-ttu-id="34896-129">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="34896-129">This sample is available in the following locations.</span></span>



| <span data-ttu-id="34896-130">Расположение</span><span class="sxs-lookup"><span data-stu-id="34896-130">Location</span></span>                                                     | <span data-ttu-id="34896-131">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="34896-131">Path/URL</span></span>                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="34896-132">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="34896-132">Windows SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=8279) | <span data-ttu-id="34896-133">*Корневой* \\ элемент SDK Примеры \\ \\ воспроизведения мультимедиа медиафаундатион \\</span><span class="sxs-lookup"><span data-stu-id="34896-133">*SDK Root*\\Samples\\multimedia\\mediafoundation\\Playlist</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="34896-134">См. также</span><span class="sxs-lookup"><span data-stu-id="34896-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="34896-135">[Пример Басикплайбакк](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34896-135">[BasicPlayback Sample](/previous-versions//bb970475(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="34896-136">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34896-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="34896-137">Источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="34896-137">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 
