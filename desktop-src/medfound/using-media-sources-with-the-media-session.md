---
description: Использование источников мультимедиа с сеансом мультимедиа
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Использование источников мультимедиа с сеансом мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999898"
---
# <a name="using-media-sources-with-the-media-session"></a><span data-ttu-id="afe3d-103">Использование источников мультимедиа с сеансом мультимедиа</span><span class="sxs-lookup"><span data-stu-id="afe3d-103">Using Media Sources with the Media Session</span></span>

<span data-ttu-id="afe3d-104">Если для управления воспроизведением используется сеанс мультимедиа, то набор методов, которые следует вызывать в источнике мультимедиа, ограничен.</span><span class="sxs-lookup"><span data-stu-id="afe3d-104">If you are using the Media Session to control playback, the set of methods that you should call on a media source is restricted.</span></span> <span data-ttu-id="afe3d-105">В этом разделе описывается, как использовать источник мультимедиа в сочетании с сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="afe3d-105">This section describes how to use media source in conjunction with the Media Session.</span></span>

<span data-ttu-id="afe3d-106">Ниже приведены основные шаги, которые будет выполнять приложение.</span><span class="sxs-lookup"><span data-stu-id="afe3d-106">Here are the basic steps your application will perform:</span></span>

1.  <span data-ttu-id="afe3d-107">Создайте источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="afe3d-107">Create the media source.</span></span> <span data-ttu-id="afe3d-108">Чтобы создать источник мультимедиа, используйте сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="afe3d-108">To create a media source, use the source resolver.</span></span> <span data-ttu-id="afe3d-109">Дополнительные сведения см. в разделе [сопоставитель источников](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="afe3d-109">For more information, see [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="afe3d-110">Сопоставитель источника возвращает указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника.</span><span class="sxs-lookup"><span data-stu-id="afe3d-110">The source resolver returns a pointer to the source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="afe3d-111">(Если вы написали пользовательский источник мультимедиа, вместо него можно предоставить пользовательский метод создания.)</span><span class="sxs-lookup"><span data-stu-id="afe3d-111">(If you have written a custom media source, you can provide a custom creation method instead.)</span></span>

2.  <span data-ttu-id="afe3d-112">Настройте презентацию.</span><span class="sxs-lookup"><span data-stu-id="afe3d-112">Configure the presentation.</span></span> <span data-ttu-id="afe3d-113">Чтобы настроить представление источника, вызовите метод [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="afe3d-113">To configure the source's presentation, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="afe3d-114">Эту копию можно изменить, но изменения не станут активными до начала воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="afe3d-114">You can modify this copy, but the changes do not become active until the playback starts.</span></span> <span data-ttu-id="afe3d-115">Не изменяйте дескриптор презентации во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="afe3d-115">Do not modify the presentation descriptor during playback.</span></span> <span data-ttu-id="afe3d-116">Дополнительные сведения см. в разделе [дескрипторы представления](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="afe3d-116">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

3.  <span data-ttu-id="afe3d-117">Создайте топологию, содержащую источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="afe3d-117">Create a topology that contains the media source.</span></span> <span data-ttu-id="afe3d-118">Дополнительные сведения см. в разделе [топологии](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="afe3d-118">For more information, see [Topologies](topologies.md).</span></span>

4.  <span data-ttu-id="afe3d-119">Используйте сеанс мультимедиа для управления воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="afe3d-119">Use the Media Session to control playback.</span></span> <span data-ttu-id="afe3d-120">Сеанс мультимедиа вызывает методы в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="afe3d-120">The Media Session calls methods on the media source.</span></span> <span data-ttu-id="afe3d-121">В настоящее время приложение не должно вызывать методы в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="afe3d-121">The application should not call any methods on the media source at this time.</span></span>

5.  <span data-ttu-id="afe3d-122">Перед освобождением источника мультимедиа вызовите [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) , чтобы завершить работу источника.</span><span class="sxs-lookup"><span data-stu-id="afe3d-122">Before releasing the media source, call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the source.</span></span>

    > [!Note]  
    > <span data-ttu-id="afe3d-123">Если вы используете источник Sequencer, источник Sequencer выполняет завершение работы источников сегмента.</span><span class="sxs-lookup"><span data-stu-id="afe3d-123">If you are using the sequencer source, the sequencer source handles shutting down the segment sources.</span></span> <span data-ttu-id="afe3d-124">Дополнительные сведения см. в разделе [источник Sequencer](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="afe3d-124">For more information, see [Sequencer Source](sequencer-source.md).</span></span>

     

<span data-ttu-id="afe3d-125">При использовании сеанса мультимедиа единственными методами, которые следует вызывать в источнике мультимедиа, являются [**креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**характеристика**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)и [**Завершение работы**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="afe3d-125">If you use the Media Session, the only methods that you should call on the media source are [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics), and [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span> <span data-ttu-id="afe3d-126">В частности:</span><span class="sxs-lookup"><span data-stu-id="afe3d-126">In particular:</span></span>

-   <span data-ttu-id="afe3d-127">Не вызывайте [**Запуск**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**приостановку**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)или [**остановку**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); Эти методы должны вызываться только сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="afe3d-127">Do not call [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause), or [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); these methods should be called only by the Media Session.</span></span>

-   <span data-ttu-id="afe3d-128">Не вызывайте ни один из методов [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .</span><span class="sxs-lookup"><span data-stu-id="afe3d-128">Do not call any [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) methods.</span></span>

-   <span data-ttu-id="afe3d-129">Не извлекать события непосредственно из источника мультимедиа или из потоков.</span><span class="sxs-lookup"><span data-stu-id="afe3d-129">Do not retrieve events directly from the media source or any of the streams.</span></span> <span data-ttu-id="afe3d-130">Сеанс мультимедиа должен получить эти события для правильной работы конвейера.</span><span class="sxs-lookup"><span data-stu-id="afe3d-130">The Media Session must receive these events for the pipeline to function correctly.</span></span> <span data-ttu-id="afe3d-131">Сеанс мультимедиа пересылает все события, необходимые для приложения.</span><span class="sxs-lookup"><span data-stu-id="afe3d-131">The Media Session forwards any events that are needed by the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afe3d-132">См. также</span><span class="sxs-lookup"><span data-stu-id="afe3d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afe3d-133">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="afe3d-133">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



