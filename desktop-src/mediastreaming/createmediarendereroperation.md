---
title: Класс Креатемедиарендерероператион
description: Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной Креатемедиарендерерасинк или Креатемедиарендерерфромбасикдевицеасинк, и предоставляет метод, возвращающий результаты операции.
ms.assetid: 0BC87D9E-5285-4F98-96B4-C841DDECBBE0
keywords:
- API потоковой передачи мультимедиа класса Креатемедиарендерероператион
- Описание API потоковой передачи мультимедиа класса Креатемедиарендерероператион
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8be789f4343779d315808a4fc5f203f62dd58c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069062"
---
# <a name="createmediarendereroperation-class"></a><span data-ttu-id="ffc10-105">Класс Креатемедиарендерероператион</span><span class="sxs-lookup"><span data-stu-id="ffc10-105">CreateMediaRendererOperation class</span></span>

<span data-ttu-id="ffc10-106">Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**креатемедиарендерерасинк**](imediarendererfactory-createmediarendererasync.md) или [**креатемедиарендерерфромбасикдевицеасинк**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) , и предоставляет метод, возвращающий результаты операции.</span><span class="sxs-lookup"><span data-stu-id="ffc10-106">Registers an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="ffc10-107">**Креатемедиарендерероператион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ffc10-107">**CreateMediaRendererOperation** has these types of members:</span></span>

-   [<span data-ttu-id="ffc10-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ffc10-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="ffc10-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffc10-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ffc10-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ffc10-110">Methods</span></span>

<span data-ttu-id="ffc10-111">Класс **креатемедиарендерероператион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ffc10-111">The **CreateMediaRendererOperation** class has these methods.</span></span>



| <span data-ttu-id="ffc10-112">Метод</span><span class="sxs-lookup"><span data-stu-id="ffc10-112">Method</span></span>                                                        | <span data-ttu-id="ffc10-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ffc10-113">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="ffc10-114">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="ffc10-114">**GetResults**</span></span>](createmediarendereroperation-getresults.md) | <span data-ttu-id="ffc10-115">Возвращает результаты асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="ffc10-115">Gets the results of the asynchronous operation.</span></span> <br/> |



 

### <a name="properties"></a><span data-ttu-id="ffc10-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffc10-116">Properties</span></span>

<span data-ttu-id="ffc10-117">Класс **креатемедиарендерероператион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ffc10-117">The **CreateMediaRendererOperation** class has these properties.</span></span>



| <span data-ttu-id="ffc10-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="ffc10-118">Property</span></span>                                                               | <span data-ttu-id="ffc10-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="ffc10-119">Access type</span></span>           | <span data-ttu-id="ffc10-120">Описание</span><span class="sxs-lookup"><span data-stu-id="ffc10-120">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffc10-121">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="ffc10-121">**Completed**</span></span>](createmediarendereroperation-completed.md)<br/> | <span data-ttu-id="ffc10-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ffc10-122">Read/write</span></span><br/> | <span data-ttu-id="ffc10-123">Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**креатемедиарендерерасинк**](imediarendererfactory-createmediarendererasync.md) или [**креатемедиарендерерфромбасикдевицеасинк**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc10-123">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span> <br/> |



 

 

 





