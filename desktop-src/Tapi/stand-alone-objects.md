---
description: В интерфейсе TAPI 3 есть несколько объектов, которые не зависят от пяти основных объектов TAPI (TAPI, адрес, вызов, Каллхуб и терминал).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Stand-Alone объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909620"
---
# <a name="stand-alone-objects"></a><span data-ttu-id="f204d-103">Stand-Alone объекты</span><span class="sxs-lookup"><span data-stu-id="f204d-103">Stand-Alone Objects</span></span>

<span data-ttu-id="f204d-104">В интерфейсе TAPI 3 есть несколько объектов, которые не зависят от пяти основных объектов TAPI (TAPI, адрес, вызов, Каллхуб и терминал).</span><span class="sxs-lookup"><span data-stu-id="f204d-104">TAPI 3 involves a number of objects that are independent of its five main TAPI objects (TAPI, Address, Call, CallHub, and Terminal).</span></span> <span data-ttu-id="f204d-105">Интерфейсы [событий](./event-interfaces.md) и [перечислителей](enumerator-interfaces.md) являются изолированными объектами и обобщены отдельно.</span><span class="sxs-lookup"><span data-stu-id="f204d-105">[Event Interfaces](./event-interfaces.md) and [Enumerator Interfaces](enumerator-interfaces.md) are stand-alone objects, and are summarized separately.</span></span> <span data-ttu-id="f204d-106">Ниже приведена сводка автономных интерфейсов, не являющихся событиями и перечислителями.</span><span class="sxs-lookup"><span data-stu-id="f204d-106">The following summarizes non-event and non-enumerator stand-alone interfaces.</span></span>



| <span data-ttu-id="f204d-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f204d-107">Interface</span></span>                                             | <span data-ttu-id="f204d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f204d-108">Description</span></span>                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f204d-109">**итколлектион**</span><span class="sxs-lookup"><span data-stu-id="f204d-109">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | <span data-ttu-id="f204d-110">Предоставляет методы, позволяющие клиентским приложениям автоматизации, таким как Visual Basic, получать сведения о коллекции.</span><span class="sxs-lookup"><span data-stu-id="f204d-110">Provides methods to allow Automation client applications such as Visual Basic to retrieve collection information.</span></span>                                                                                             |
| [<span data-ttu-id="f204d-111">**ITCollection2**</span><span class="sxs-lookup"><span data-stu-id="f204d-111">**ITCollection2**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | <span data-ttu-id="f204d-112">Расширяет [**итколлектион**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) , предоставляя дополнительные методы для изменения коллекций.</span><span class="sxs-lookup"><span data-stu-id="f204d-112">Extends [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) by providing additional methods for modifying collections.</span></span>                                                                                                       |
| [<span data-ttu-id="f204d-113">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="f204d-113">**IDispatch**</span></span>](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | <span data-ttu-id="f204d-114">Стандартный COM-интерфейс для реализации автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f204d-114">Standard COM interface for implementing Automation.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="f204d-115">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="f204d-115">**IUnknown**</span></span>](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | <span data-ttu-id="f204d-116">Стандартный COM-интерфейс для получения указателей на интерфейсы объектов.</span><span class="sxs-lookup"><span data-stu-id="f204d-116">Standard COM interface for getting pointers to object interfaces.</span></span>                                                                                                                                             |
| [<span data-ttu-id="f204d-117">**итдиспатчмаппер**</span><span class="sxs-lookup"><span data-stu-id="f204d-117">**ITDispatchMapper**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | <span data-ttu-id="f204d-118">Позволяет приложению извлекать указатель диспетчеризации другого интерфейса объекта, учитывая текущий указатель [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) .</span><span class="sxs-lookup"><span data-stu-id="f204d-118">Allows an application to retrieve the dispatch pointer of another interface on an object, given a current [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) pointer.</span></span> <span data-ttu-id="f204d-119">Полезно для некоторых языков сценариев.</span><span class="sxs-lookup"><span data-stu-id="f204d-119">Useful for some scripting languages.</span></span> |
| [<span data-ttu-id="f204d-120">**итрекуест**</span><span class="sxs-lookup"><span data-stu-id="f204d-120">**ITRequest**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | <span data-ttu-id="f204d-121">Предоставляет методы, позволяющие приложениям TAPI 3 использовать [телефонные телефония](assisted-telephony-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f204d-121">Provides methods that allow a TAPI 3 application to use [Assisted Telephony](assisted-telephony-overview.md).</span></span>                                                                                                |



 



| <span data-ttu-id="f204d-122">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f204d-122">Interface</span></span>                                  | <span data-ttu-id="f204d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="f204d-123">Description</span></span>                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f204d-124">**итмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="f204d-124">**ITMediaControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | <span data-ttu-id="f204d-125">Запускает, останавливает и приостанавливает текущие действия, например воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="f204d-125">Starts, stops, and pauses current actions, such as a playback.</span></span>                                                                                                             |
| [<span data-ttu-id="f204d-126">**итмедиаплайбакк**</span><span class="sxs-lookup"><span data-stu-id="f204d-126">**ITMediaPlayback**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | <span data-ttu-id="f204d-127">Предоставляет методы для воспроизведения, позволяющие приложению выполнять такие операции, как установка списка файлов для воспроизведения и изменение скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f204d-127">Provides playback-specific methods that allow an application to perform such operations as setting the list of files to play and changing the playback speed.</span></span>              |
| [<span data-ttu-id="f204d-128">**итмедиарекорд**</span><span class="sxs-lookup"><span data-stu-id="f204d-128">**ITMediaRecord**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | <span data-ttu-id="f204d-129">Предоставляет методы записи, позволяющие приложению выполнять такие операции, как задание имен файлов для записи и изменения длительности записи.</span><span class="sxs-lookup"><span data-stu-id="f204d-129">Provides recording-specific methods that allow an application to perform such operations as setting the names of files to record and changing the duration of a recording.</span></span> |



 



| <span data-ttu-id="f204d-130">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f204d-130">Interface</span></span>                                                  | <span data-ttu-id="f204d-131">Описание</span><span class="sxs-lookup"><span data-stu-id="f204d-131">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f204d-132">**итскриптаблеаудиоформат**</span><span class="sxs-lookup"><span data-stu-id="f204d-132">**ITScriptableAudioFormat**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | <span data-ttu-id="f204d-133">Извлекает формат аудио из или задает звуковой формат для дорожки.</span><span class="sxs-lookup"><span data-stu-id="f204d-133">Retrieves the audio format from, or sets the audio format for, a track.</span></span>                                                                                             |
| [<span data-ttu-id="f204d-134">**итстатикаудиотерминал**</span><span class="sxs-lookup"><span data-stu-id="f204d-134">**ITStaticAudioTerminal**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | <span data-ttu-id="f204d-135">Предоставляет методы для статических объектов аудио терминала, которые необходимы для поддержки телефонных устройств.</span><span class="sxs-lookup"><span data-stu-id="f204d-135">Provides methods on static audio terminal objects that are needed to support phone devices.</span></span> <span data-ttu-id="f204d-136">TAPI 3,1 MSP должен предоставлять этот интерфейс во всех статических звуковых терминалах.</span><span class="sxs-lookup"><span data-stu-id="f204d-136">TAPI 3.1 MSPs must expose this interface on all static audio terminals.</span></span> |



 

 

 
