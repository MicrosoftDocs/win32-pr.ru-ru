---
title: Класс Жетмутеоператион
description: Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной Жетмутеасинк, и предоставляет метод, возвращающий результаты операции. | Класс Жетмутеоператион
ms.assetid: 691D4936-604A-496F-B62E-FB36B406F0DD
keywords:
- API потоковой передачи мультимедиа класса Жетмутеоператион
- Описание API потоковой передачи мультимедиа класса Жетмутеоператион
topic_type:
- apiref
api_name:
- GetMuteOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b75758dc2383cf237da90c38f6a2efdbf6754e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684928"
---
# <a name="getmuteoperation-class"></a><span data-ttu-id="a6dd5-106">Класс Жетмутеоператион</span><span class="sxs-lookup"><span data-stu-id="a6dd5-106">GetMuteOperation class</span></span>

<span data-ttu-id="a6dd5-107">Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) , и предоставляет метод, возвращающий результаты операции.</span><span class="sxs-lookup"><span data-stu-id="a6dd5-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="a6dd5-108">**Жетмутеоператион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a6dd5-108">**GetMuteOperation** has these types of members:</span></span>

-   [<span data-ttu-id="a6dd5-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a6dd5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a6dd5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a6dd5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a6dd5-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a6dd5-111">Methods</span></span>

<span data-ttu-id="a6dd5-112">Класс **жетмутеоператион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a6dd5-112">The **GetMuteOperation** class has these methods.</span></span>



| <span data-ttu-id="a6dd5-113">Метод</span><span class="sxs-lookup"><span data-stu-id="a6dd5-113">Method</span></span>                                            | <span data-ttu-id="a6dd5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a6dd5-114">Description</span></span>                                                                                                                   |
|:--------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6dd5-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="a6dd5-115">**GetResults**</span></span>](getmuteoperation-getresults.md) | <span data-ttu-id="a6dd5-116">Возвращает результаты асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span><span class="sxs-lookup"><span data-stu-id="a6dd5-116">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span> <br/> |



 

### <a name="properties"></a><span data-ttu-id="a6dd5-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="a6dd5-117">Properties</span></span>

<span data-ttu-id="a6dd5-118">Класс **жетмутеоператион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a6dd5-118">The **GetMuteOperation** class has these properties.</span></span>



| <span data-ttu-id="a6dd5-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="a6dd5-119">Property</span></span>                                                   | <span data-ttu-id="a6dd5-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="a6dd5-120">Access type</span></span>           | <span data-ttu-id="a6dd5-121">Описание</span><span class="sxs-lookup"><span data-stu-id="a6dd5-121">Description</span></span>                                                                                                                                                            |
|:-----------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6dd5-122">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="a6dd5-122">**Completed**</span></span>](getmuteoperation-completed.md)<br/> | <span data-ttu-id="a6dd5-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="a6dd5-123">Read/write</span></span><br/> | <span data-ttu-id="a6dd5-124">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) .</span><span class="sxs-lookup"><span data-stu-id="a6dd5-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span> <br/> |



 

 

