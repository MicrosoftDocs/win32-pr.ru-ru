---
title: Класс Жеттранспортинформатионоператион
description: Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной Жеттранспортинформатионасинк, и предоставляет метод, возвращающий результаты операции.
ms.assetid: EDB7E338-94E9-47DA-A95E-E49123655505
keywords:
- API потоковой передачи мультимедиа класса Жеттранспортинформатионоператион
- Описание API потоковой передачи мультимедиа класса Жеттранспортинформатионоператион
topic_type:
- apiref
api_name:
- GetTransportInformationOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05d1eee0dd415e22fb7caaac2c4fc60e53344ba8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533143"
---
# <a name="gettransportinformationoperation-class"></a><span data-ttu-id="ca981-105">Класс Жеттранспортинформатионоператион</span><span class="sxs-lookup"><span data-stu-id="ca981-105">GetTransportInformationOperation class</span></span>

<span data-ttu-id="ca981-106">Регистрирует обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) , и предоставляет метод, возвращающий результаты операции.</span><span class="sxs-lookup"><span data-stu-id="ca981-106">Registers an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="ca981-107">**Жеттранспортинформатионоператион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ca981-107">**GetTransportInformationOperation** has these types of members:</span></span>

-   [<span data-ttu-id="ca981-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ca981-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca981-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca981-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca981-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ca981-110">Methods</span></span>

<span data-ttu-id="ca981-111">Класс **жеттранспортинформатионоператион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ca981-111">The **GetTransportInformationOperation** class has these methods.</span></span>



| <span data-ttu-id="ca981-112">Метод</span><span class="sxs-lookup"><span data-stu-id="ca981-112">Method</span></span>                                                            | <span data-ttu-id="ca981-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ca981-113">Description</span></span>                                                                                                                                                  |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca981-114">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="ca981-114">**GetResults**</span></span>](gettransportinformationoperation-getresults.md) | <span data-ttu-id="ca981-115">Возвращает результаты асинхронной операции, запущенной [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span><span class="sxs-lookup"><span data-stu-id="ca981-115">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ca981-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca981-116">Properties</span></span>

<span data-ttu-id="ca981-117">Класс **жеттранспортинформатионоператион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ca981-117">The **GetTransportInformationOperation** class has these properties.</span></span>



| <span data-ttu-id="ca981-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="ca981-118">Property</span></span>                                                                   | <span data-ttu-id="ca981-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="ca981-119">Access type</span></span>           | <span data-ttu-id="ca981-120">Описание</span><span class="sxs-lookup"><span data-stu-id="ca981-120">Description</span></span>                                                                                                                                                                                            |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca981-121">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="ca981-121">**Completed**</span></span>](gettransportinformationoperation-completed.md)<br/> | <span data-ttu-id="ca981-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ca981-122">Read/write</span></span><br/> | <span data-ttu-id="ca981-123">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) .</span><span class="sxs-lookup"><span data-stu-id="ca981-123">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span> <br/> |



 

 

