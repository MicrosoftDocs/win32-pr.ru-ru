---
description: Интерфейсы для построения графов фильтра
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Интерфейсы для построения графов фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805657"
---
# <a name="interfaces-for-building-filter-graphs"></a><span data-ttu-id="439d1-103">Интерфейсы для построения графов фильтра</span><span class="sxs-lookup"><span data-stu-id="439d1-103">Interfaces for Building Filter Graphs</span></span>

<span data-ttu-id="439d1-104">Приложения используют эти интерфейсы для создания различных типов графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="439d1-104">Applications use these interfaces to build various types of filter graphs.</span></span>



| <span data-ttu-id="439d1-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="439d1-105">Interface</span></span>                                                  | <span data-ttu-id="439d1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="439d1-106">Description</span></span>                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="439d1-107">**иамфилтерграфкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="439d1-107">**IAMFilterGraphCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | <span data-ttu-id="439d1-108">Получение уведомлений обратного вызова, если не удается отобразить ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="439d1-108">Receive callback notifications if a pin cannot be rendered.</span></span> |
| [<span data-ttu-id="439d1-109">**иамграфбуилдеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="439d1-109">**IAMGraphBuilderCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | <span data-ttu-id="439d1-110">Предоставляет механизм обратного вызова во время построения графа.</span><span class="sxs-lookup"><span data-stu-id="439d1-110">Provides a callback mechanism during graph building.</span></span>        |
| [<span data-ttu-id="439d1-111">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="439d1-111">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | <span data-ttu-id="439d1-112">Создание графов фильтра для видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="439d1-112">Build filter graphs for video capture.</span></span>                      |
| [<span data-ttu-id="439d1-113">**икреатедевенум**</span><span class="sxs-lookup"><span data-stu-id="439d1-113">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | <span data-ttu-id="439d1-114">Перечисление системных устройств, таких как устройства записи.</span><span class="sxs-lookup"><span data-stu-id="439d1-114">Enumerate system devices, such as capture devices.</span></span>          |
| [<span data-ttu-id="439d1-115">**идвдграфбуилдер**</span><span class="sxs-lookup"><span data-stu-id="439d1-115">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | <span data-ttu-id="439d1-116">Создание графов фильтра для навигации и воспроизведения DVD.</span><span class="sxs-lookup"><span data-stu-id="439d1-116">Build filter graphs for DVD navigation and playback.</span></span>        |
| [<span data-ttu-id="439d1-117">**иенумфилтерс**</span><span class="sxs-lookup"><span data-stu-id="439d1-117">**IEnumFilters**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | <span data-ttu-id="439d1-118">Перечисление фильтров в графе.</span><span class="sxs-lookup"><span data-stu-id="439d1-118">Enumerate the filters in the graph.</span></span>                         |
| [<span data-ttu-id="439d1-119">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="439d1-119">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | <span data-ttu-id="439d1-120">Добавление, удаление или подключение фильтров.</span><span class="sxs-lookup"><span data-stu-id="439d1-120">Add, remove, or connect filters.</span></span>                            |
| [<span data-ttu-id="439d1-121">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="439d1-121">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | <span data-ttu-id="439d1-122">Перечисление фильтров, зарегистрированных в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="439d1-122">Enumerate the filters registered on the user's system.</span></span>      |
| [<span data-ttu-id="439d1-123">**играфбуилдер**</span><span class="sxs-lookup"><span data-stu-id="439d1-123">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | <span data-ttu-id="439d1-124">Построить графы фильтра для воспроизведения файлов или для пользовательских целей.</span><span class="sxs-lookup"><span data-stu-id="439d1-124">Build filter graphs for file playback or for custom uses.</span></span>   |
| [<span data-ttu-id="439d1-125">**играфконфиг**</span><span class="sxs-lookup"><span data-stu-id="439d1-125">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | <span data-ttu-id="439d1-126">Динамически перенастройте граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="439d1-126">Dynamically reconfigure a filter graph.</span></span>                     |
| [<span data-ttu-id="439d1-127">**играфверсион**</span><span class="sxs-lookup"><span data-stu-id="439d1-127">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | <span data-ttu-id="439d1-128">Определить, когда граф изменится.</span><span class="sxs-lookup"><span data-stu-id="439d1-128">Determine when the graph changes.</span></span>                           |



 

 

 



