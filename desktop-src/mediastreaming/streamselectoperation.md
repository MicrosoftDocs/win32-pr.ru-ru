---
title: Класс Стреамселектоператион
description: Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной Жетмутеасинк, и предоставляет метод, возвращающий результаты операции. | Класс Стреамселектоператион
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- API потоковой передачи мультимедиа класса Стреамселектоператион
- Описание API потоковой передачи мультимедиа класса Стреамселектоператион
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273551"
---
# <a name="streamselectoperation-class"></a><span data-ttu-id="b8d5f-106">Класс Стреамселектоператион</span><span class="sxs-lookup"><span data-stu-id="b8d5f-106">StreamSelectOperation class</span></span>

<span data-ttu-id="b8d5f-107">Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) , и предоставляет метод, возвращающий результаты операции.</span><span class="sxs-lookup"><span data-stu-id="b8d5f-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="b8d5f-108">**Стреамселектоператион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b8d5f-108">**StreamSelectOperation** has these types of members:</span></span>

-   [<span data-ttu-id="b8d5f-109">Методы</span><span class="sxs-lookup"><span data-stu-id="b8d5f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8d5f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8d5f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8d5f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="b8d5f-111">Methods</span></span>

<span data-ttu-id="b8d5f-112">Класс **стреамселектоператион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b8d5f-112">The **StreamSelectOperation** class has these methods.</span></span>



| <span data-ttu-id="b8d5f-113">Метод</span><span class="sxs-lookup"><span data-stu-id="b8d5f-113">Method</span></span>                                                 | <span data-ttu-id="b8d5f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b8d5f-114">Description</span></span>                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8d5f-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="b8d5f-115">**GetResults**</span></span>](streamselectoperation-getresults.md) | <span data-ttu-id="b8d5f-116">Возвращает результаты асинхронной операции, запущенной [**селектбестстреамасинк**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8d5f-116">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8d5f-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8d5f-117">Properties</span></span>

<span data-ttu-id="b8d5f-118">Класс **стреамселектоператион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b8d5f-118">The **StreamSelectOperation** class has these properties.</span></span>



| <span data-ttu-id="b8d5f-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="b8d5f-119">Property</span></span>                                                        | <span data-ttu-id="b8d5f-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b8d5f-120">Access type</span></span>           | <span data-ttu-id="b8d5f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="b8d5f-121">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8d5f-122">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="b8d5f-122">**Completed**</span></span>](streamselectoperation-completed.md)<br/> | <span data-ttu-id="b8d5f-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="b8d5f-123">Read/write</span></span><br/> | <span data-ttu-id="b8d5f-124">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**селектбестстреамасинк**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8d5f-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span><br/> |



 

 

