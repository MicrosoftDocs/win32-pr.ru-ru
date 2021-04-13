---
description: Создание расширенной топологии
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Создание расширенной топологии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343335"
---
# <a name="advanced-topology-building"></a><span data-ttu-id="7ad83-103">Создание расширенной топологии</span><span class="sxs-lookup"><span data-stu-id="7ad83-103">Advanced Topology Building</span></span>

<span data-ttu-id="7ad83-104">В этом разделе описываются некоторые дополнительные методы создания топологий.</span><span class="sxs-lookup"><span data-stu-id="7ad83-104">This section describes some advanced techniques for building topologies.</span></span> <span data-ttu-id="7ad83-105">Эти методы можно использовать, если требуется больший контроль над топологиями, которые вы отправляете в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7ad83-105">You can use these techniques if you want more control over the topologies that you send to the Media Session.</span></span>

<span data-ttu-id="7ad83-106">Так как эти методы предназначены для сценариев, которые выходят за рамки функций стандартного загрузчика топологии, многие сведения будут зависеть от конкретных требований приложения.</span><span class="sxs-lookup"><span data-stu-id="7ad83-106">Because these techniques are intended for scenarios that go beyond the functionality provided by the standard topology loader, many of the details will depend on the particular requirements of your application.</span></span> <span data-ttu-id="7ad83-107">Таким образом, этот раздел организован вокруг небольших подзадач, а не полных комплексных сценариев.</span><span class="sxs-lookup"><span data-stu-id="7ad83-107">Therefore, this section is organized loosely around smaller subtasks, rather than complete, end-to-end scenarios.</span></span>

<span data-ttu-id="7ad83-108">Типичное приложение воспроизведения выполняется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="7ad83-108">The typical playback application follows these steps:</span></span>

1.  <span data-ttu-id="7ad83-109">Приложение создает частичную топологию и помещает ее в очередь в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7ad83-109">The application builds a partial topology and queues it on the Media Session.</span></span>
2.  <span data-ttu-id="7ad83-110">Сеанс мультимедиа вызывает загрузчик топологии для разрешения топологии.</span><span class="sxs-lookup"><span data-stu-id="7ad83-110">The Media Session invokes the topology loader to resolve the topology.</span></span>

<span data-ttu-id="7ad83-111">Если вы хотите выйти за пределы возможностей загрузчика топологии, существуют три общих подхода.</span><span class="sxs-lookup"><span data-stu-id="7ad83-111">If you want to go beyond the capabilities of the topology loader, there are three general approaches:</span></span>

-   <span data-ttu-id="7ad83-112">Создайте полную топологию.</span><span class="sxs-lookup"><span data-stu-id="7ad83-112">Build a complete topology.</span></span> <span data-ttu-id="7ad83-113">При постановке топологии в очередь в сеансе мультимедиа вызовите [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) с \_ флагом МФСЕССИОН сеттопологи без \_ разрешения.</span><span class="sxs-lookup"><span data-stu-id="7ad83-113">When you queue the topology on the Media Session, call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the MFSESSION\_SETTOPOLOGY\_NORESOLUTION flag.</span></span> <span data-ttu-id="7ad83-114">Этот флаг предотвращает попытку сеанса мультимедиа разрешить топологию.</span><span class="sxs-lookup"><span data-stu-id="7ad83-114">This flag prevents the Media Session from attempting to resolve the topology.</span></span>

-   <span data-ttu-id="7ad83-115">Чтобы разрешить топологию, непосредственно запустите загрузчик топологии.</span><span class="sxs-lookup"><span data-stu-id="7ad83-115">Directly invoke the topology loader to resolve the topology.</span></span> <span data-ttu-id="7ad83-116">Затем можно изменить полную топологию, прежде чем поставить ее в очередь в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7ad83-116">You can then modify the full topology before queuing it on the Media Session.</span></span>

-   <span data-ttu-id="7ad83-117">Реализуйте пользовательский загрузчик топологии.</span><span class="sxs-lookup"><span data-stu-id="7ad83-117">Implement a custom topology loader.</span></span> <span data-ttu-id="7ad83-118">При таком подходе вы помещаете в очередь частичную топологию, но сеанс мультимедиа вызывает пользовательский загрузчик вместо стандартной реализации Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7ad83-118">With this approach, you queue a partial topology, but the Media Session invokes your custom loader instead of the standard Media Foundation implementation.</span></span> <span data-ttu-id="7ad83-119">Одним из преимуществ такого подхода является то, что вы можете создавать пользовательские топологии в защищенной среде.</span><span class="sxs-lookup"><span data-stu-id="7ad83-119">One advantage of this approach is that you can perform custom topology building inside the protected environment.</span></span> <span data-ttu-id="7ad83-120">(В этом случае загрузчик топологии должен быть доверенным компонентом.</span><span class="sxs-lookup"><span data-stu-id="7ad83-120">(In that case, however, the topology loader must be a trusted component.</span></span> <span data-ttu-id="7ad83-121">Дополнительные сведения см. в разделе [путь к защищенному носителю](protected-media-path.md).)</span><span class="sxs-lookup"><span data-stu-id="7ad83-121">For more information, see [Protected Media Path](protected-media-path.md).)</span></span>

<span data-ttu-id="7ad83-122">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="7ad83-122">This section contains the following topics.</span></span>



| <span data-ttu-id="7ad83-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ad83-123">Topic</span></span>                                                                          | <span data-ttu-id="7ad83-124">Описание</span><span class="sxs-lookup"><span data-stu-id="7ad83-124">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ad83-125">Пользовательские загрузчики топологии</span><span class="sxs-lookup"><span data-stu-id="7ad83-125">Custom Topology Loaders</span></span>](custom-topology-loaders.md)                         | <span data-ttu-id="7ad83-126">Как предоставить пользовательскую реализацию [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7ad83-126">How to provide a custom implementation of [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) for the Media Session.</span></span>          |
| [<span data-ttu-id="7ad83-127">Привязка выходных узлов к приемникам мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7ad83-127">Binding Output Nodes to Media Sinks</span></span>](binding-output-nodes-to-media-sinks.md) | <span data-ttu-id="7ad83-128">Как подготовить выходные узлы в топологии, если вы используете загрузчик топологии за пределами сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7ad83-128">How to prepare the output nodes in a topology if you are using the topology loader outside of the Media Session.</span></span> |
| [<span data-ttu-id="7ad83-129">Добавление декодера в топологию</span><span class="sxs-lookup"><span data-stu-id="7ad83-129">Adding a Decoder to a Topology</span></span>](adding-a-decoder-to-a-topology.md)           | <span data-ttu-id="7ad83-130">Выбор декодера вручную и добавление его в топологию.</span><span class="sxs-lookup"><span data-stu-id="7ad83-130">How to select a decoder manually and add it to a topology.</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="7ad83-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7ad83-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ad83-132">Топологии</span><span class="sxs-lookup"><span data-stu-id="7ad83-132">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



