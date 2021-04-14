---
title: Класс Жетпоситионинформатионоператион
description: Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной Жетпоситионинформатионасинк, и предоставляет метод, возвращающий результаты операции.
ms.assetid: 57DDE3B2-EFA9-4FEB-B701-D987C58F5CEA
keywords:
- API потоковой передачи мультимедиа класса Жетпоситионинформатионоператион
- Описание API потоковой передачи мультимедиа класса Жетпоситионинформатионоператион
topic_type:
- apiref
api_name:
- GetPositionInformationOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d62de60e1e3f7f2965b1248e173ed9962b73361d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487664"
---
# <a name="getpositioninformationoperation-class"></a><span data-ttu-id="280a7-105">Класс Жетпоситионинформатионоператион</span><span class="sxs-lookup"><span data-stu-id="280a7-105">GetPositionInformationOperation class</span></span>

<span data-ttu-id="280a7-106">Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) , и предоставляет метод, возвращающий результаты операции.</span><span class="sxs-lookup"><span data-stu-id="280a7-106">Registers an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="280a7-107">**Жетпоситионинформатионоператион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="280a7-107">**GetPositionInformationOperation** has these types of members:</span></span>

-   [<span data-ttu-id="280a7-108">Методы</span><span class="sxs-lookup"><span data-stu-id="280a7-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="280a7-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="280a7-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="280a7-110">Методы</span><span class="sxs-lookup"><span data-stu-id="280a7-110">Methods</span></span>

<span data-ttu-id="280a7-111">Класс **жетпоситионинформатионоператион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="280a7-111">The **GetPositionInformationOperation** class has these methods.</span></span>



| <span data-ttu-id="280a7-112">Метод</span><span class="sxs-lookup"><span data-stu-id="280a7-112">Method</span></span>                                                           | <span data-ttu-id="280a7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="280a7-113">Description</span></span>                                                                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="280a7-114">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="280a7-114">**GetResults**</span></span>](getpositioninformationoperation-getresults.md) | <span data-ttu-id="280a7-115">Возвращает результаты асинхронной операции, запущенной [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span><span class="sxs-lookup"><span data-stu-id="280a7-115">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span> <br/> |



 

### <a name="properties"></a><span data-ttu-id="280a7-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="280a7-116">Properties</span></span>

<span data-ttu-id="280a7-117">Класс **жетпоситионинформатионоператион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="280a7-117">The **GetPositionInformationOperation** class has these properties.</span></span>



| <span data-ttu-id="280a7-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="280a7-118">Property</span></span>                                                                  | <span data-ttu-id="280a7-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="280a7-119">Access type</span></span>           | <span data-ttu-id="280a7-120">Описание</span><span class="sxs-lookup"><span data-stu-id="280a7-120">Description</span></span>                                                                                                                                                                                          |
|:--------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="280a7-121">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="280a7-121">**Completed**</span></span>](getpositioninformationoperation-completed.md)<br/> | <span data-ttu-id="280a7-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="280a7-122">Read/write</span></span><br/> | <span data-ttu-id="280a7-123">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) .</span><span class="sxs-lookup"><span data-stu-id="280a7-123">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) is completed.</span></span> <br/> |



 

 

