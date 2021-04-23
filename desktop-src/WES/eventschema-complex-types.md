---
title: Сложные типы схемы событий
description: Ниже приведены сложные типы, определяемые схемой событий.
ms.assetid: bc995483-7e54-4224-a372-4e63b0dd764c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2844fef209aedf6819aeaa5a5b6b8a2d698b39a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691360"
---
# <a name="event-schema-complex-types"></a><span data-ttu-id="3bf07-103">Сложные типы схемы событий</span><span class="sxs-lookup"><span data-stu-id="3bf07-103">Event Schema Complex Types</span></span>

<span data-ttu-id="3bf07-104">Ниже приведены сложные типы, определяемые схемой событий.</span><span class="sxs-lookup"><span data-stu-id="3bf07-104">The following are the complex types that the Event schema defines.</span></span>



| <span data-ttu-id="3bf07-105">Сложный тип</span><span class="sxs-lookup"><span data-stu-id="3bf07-105">Complex type</span></span>                                                                       | <span data-ttu-id="3bf07-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3bf07-106">Description</span></span>                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3bf07-107">**комплексдататипе**</span><span class="sxs-lookup"><span data-stu-id="3bf07-107">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md)                 | <span data-ttu-id="3bf07-108">Определяет структуру, содержащую один или несколько элементов данных.</span><span class="sxs-lookup"><span data-stu-id="3bf07-108">Defines a structure that contains one or more data items.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="3bf07-109">**DataType**</span><span class="sxs-lookup"><span data-stu-id="3bf07-109">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)                          | <span data-ttu-id="3bf07-110">Определяет элемент данных.</span><span class="sxs-lookup"><span data-stu-id="3bf07-110">Defines a data item.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="3bf07-111">**дебугдататипе**</span><span class="sxs-lookup"><span data-stu-id="3bf07-111">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="3bf07-112">Определяет данные, которые могут регистрироваться для событий препроцессора трассировки программного обеспечения Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="3bf07-112">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="3bf07-113">**евентдататипе**</span><span class="sxs-lookup"><span data-stu-id="3bf07-113">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="3bf07-114">Определяет элементы данных событий и структуры, содержащие данные события.</span><span class="sxs-lookup"><span data-stu-id="3bf07-114">Defines the event data items and structures that contains the event data.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="3bf07-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="3bf07-115">**EventType**</span></span>](eventschema-eventtype-complextype.md)                             | <span data-ttu-id="3bf07-116">Определяет корневой узел схемы событий.</span><span class="sxs-lookup"><span data-stu-id="3bf07-116">Defines the root node of the Event schema.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="3bf07-117">**процессинжеррордататипе**</span><span class="sxs-lookup"><span data-stu-id="3bf07-117">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="3bf07-118">Определяет ошибку, которая произошла во время отображения данных события для события.</span><span class="sxs-lookup"><span data-stu-id="3bf07-118">Defines an error that occurred while rendering the event data for the event.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="3bf07-119">**рендерингинфотипе**</span><span class="sxs-lookup"><span data-stu-id="3bf07-119">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="3bf07-120">Определяет отрисованные сообщения для события.</span><span class="sxs-lookup"><span data-stu-id="3bf07-120">Defines the rendered messages for the event.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="3bf07-121">**системпропертиестипе**</span><span class="sxs-lookup"><span data-stu-id="3bf07-121">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="3bf07-122">Определяет сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.</span><span class="sxs-lookup"><span data-stu-id="3bf07-122">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/> |
| [<span data-ttu-id="3bf07-123">**усердататипе**</span><span class="sxs-lookup"><span data-stu-id="3bf07-123">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="3bf07-124">Определяет фрагмент XML, указывающий макет данных события.</span><span class="sxs-lookup"><span data-stu-id="3bf07-124">Defines an XML fragment that specifies the layout of the event data.</span></span><br/>                                                                                                                           |



 

 

 





