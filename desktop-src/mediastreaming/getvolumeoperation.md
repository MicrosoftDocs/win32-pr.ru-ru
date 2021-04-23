---
title: Класс Жетволумеоператион
description: Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной Жетволумеасинк, и предоставляет метод, возвращающий результаты операции.
ms.assetid: F7BCE2AB-89B5-44CE-8BDF-347F2E3FD6C9
keywords:
- API потоковой передачи мультимедиа класса Жетволумеоператион
- Описание API потоковой передачи мультимедиа класса Жетволумеоператион
topic_type:
- apiref
api_name:
- GetVolumeOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ac06bfb85e8ebbf10306da43cb44c7e3b3e862a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691502"
---
# <a name="getvolumeoperation-class"></a><span data-ttu-id="39dd4-105">Класс Жетволумеоператион</span><span class="sxs-lookup"><span data-stu-id="39dd4-105">GetVolumeOperation class</span></span>

<span data-ttu-id="39dd4-106">Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**жетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) , и предоставляет метод, возвращающий результаты операции.</span><span class="sxs-lookup"><span data-stu-id="39dd4-106">Registers an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="39dd4-107">**Жетволумеоператион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39dd4-107">**GetVolumeOperation** has these types of members:</span></span>

-   [<span data-ttu-id="39dd4-108">Методы</span><span class="sxs-lookup"><span data-stu-id="39dd4-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="39dd4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="39dd4-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39dd4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="39dd4-110">Methods</span></span>

<span data-ttu-id="39dd4-111">Класс **жетволумеоператион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="39dd4-111">The **GetVolumeOperation** class has these methods.</span></span>



| <span data-ttu-id="39dd4-112">Метод</span><span class="sxs-lookup"><span data-stu-id="39dd4-112">Method</span></span>                                              | <span data-ttu-id="39dd4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="39dd4-113">Description</span></span>                                                                                                                      |
|:----------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39dd4-114">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="39dd4-114">**GetResults**</span></span>](getvolumeoperation-getresults.md) | <span data-ttu-id="39dd4-115">Возвращает результаты асинхронной операции, запущенной [**жетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span><span class="sxs-lookup"><span data-stu-id="39dd4-115">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="39dd4-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="39dd4-116">Properties</span></span>

<span data-ttu-id="39dd4-117">Класс **жетволумеоператион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39dd4-117">The **GetVolumeOperation** class has these properties.</span></span>



| <span data-ttu-id="39dd4-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="39dd4-118">Property</span></span>                                                     | <span data-ttu-id="39dd4-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="39dd4-119">Access type</span></span>           | <span data-ttu-id="39dd4-120">Описание</span><span class="sxs-lookup"><span data-stu-id="39dd4-120">Description</span></span>                                                                                                                                                                |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39dd4-121">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="39dd4-121">**Completed**</span></span>](getvolumeoperation-completed.md)<br/> | <span data-ttu-id="39dd4-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="39dd4-122">Read/write</span></span><br/> | <span data-ttu-id="39dd4-123">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) .</span><span class="sxs-lookup"><span data-stu-id="39dd4-123">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span> <br/> |



 

 

