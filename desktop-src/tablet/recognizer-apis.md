---
description: 'Распознаватель обрабатывает:'
ms.assetid: d7c694a2-0da6-4172-b434-2b0f94e1b649
title: Справочник по распознавателю
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e193b6098f6d82751951d1a39630ad30023c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081538"
---
# <a name="recognizer-reference"></a><span data-ttu-id="d8de3-103">Справочник по распознавателю</span><span class="sxs-lookup"><span data-stu-id="d8de3-103">Recognizer Reference</span></span>

<span data-ttu-id="d8de3-104">Распознаватель обрабатывает:</span><span class="sxs-lookup"><span data-stu-id="d8de3-104">The recognizer handles:</span></span>

-   <span data-ttu-id="d8de3-105">Определите, какие распознаватели доступны на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d8de3-105">Determine which recognizers are available on the computer.</span></span>
-   <span data-ttu-id="d8de3-106">Укажите, какой распознаватель следует использовать.</span><span class="sxs-lookup"><span data-stu-id="d8de3-106">Identify which recognizer to use.</span></span>
-   <span data-ttu-id="d8de3-107">Создайте контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d8de3-107">Create a recognizer context.</span></span>
-   <span data-ttu-id="d8de3-108">Получение результатов и альтернатив распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d8de3-108">Retrieve recognizer results and alternates.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d8de3-109">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="d8de3-109">In This Section</span></span>



| <span data-ttu-id="d8de3-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="d8de3-110">Topic</span></span>                                                      | <span data-ttu-id="d8de3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d8de3-111">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8de3-112">ХРЕКОАЛТ, обработчик</span><span class="sxs-lookup"><span data-stu-id="d8de3-112">HRECOALT Handle</span></span>](hrecoalt-handle.md)                     | <span data-ttu-id="d8de3-113">Извлекает альтернативные значения строки и свойства, такие как уровень достоверности и метрики.</span><span class="sxs-lookup"><span data-stu-id="d8de3-113">Retrieves the alternate string and property values, such as confidence level and metrics.</span></span><br/>                                                                  |
| [<span data-ttu-id="d8de3-114">ХРЕКОКОНТЕКСТ, обработчик</span><span class="sxs-lookup"><span data-stu-id="d8de3-114">HRECOCONTEXT Handle</span></span>](hrecocontext-handle.md)             | <span data-ttu-id="d8de3-115">Добавляет рукописный ввод в контекст, выполняет распознавание рукописного текста и получает результаты распознавания и альтернативные варианты.</span><span class="sxs-lookup"><span data-stu-id="d8de3-115">Adds ink to the context, performs ink recognition, and retrieves the recognition result and alternates.</span></span><br/>                                                    |
| [<span data-ttu-id="d8de3-116">ХРЕКОГНИЗЕР, обработчик</span><span class="sxs-lookup"><span data-stu-id="d8de3-116">HRECOGNIZER Handle</span></span>](hrecognizer-handle.md)               | <span data-ttu-id="d8de3-117">Создает контекст распознавателя, извлекает его атрибуты и свойства, а также определяет, какие свойства пакетов должен выполнять распознавание распознавателем.</span><span class="sxs-lookup"><span data-stu-id="d8de3-117">Creates a recognizer context, retrieves its attributes and properties, and determines which packet properties the recognizer needs to perform recognition.</span></span><br/> |
| [<span data-ttu-id="d8de3-118">ХРЕКОВОРДЛИСТ, обработчик</span><span class="sxs-lookup"><span data-stu-id="d8de3-118">HRECOWORDLIST Handle</span></span>](hrecowordlist-handle.md)           | <span data-ttu-id="d8de3-119">Управляет списком слов, который присоединяется к контексту распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d8de3-119">Manages a word list that you attach to a recognizer context.</span></span> <span data-ttu-id="d8de3-120">Этот список улучшает результаты распознавания.</span><span class="sxs-lookup"><span data-stu-id="d8de3-120">This list improves the recognition results.</span></span><br/>                                                   |
| [<span data-ttu-id="d8de3-121">Перечисления модуля распознавания</span><span class="sxs-lookup"><span data-stu-id="d8de3-121">Recognizer Enumerations</span></span>](recognizer-api-enumerations.md) | <span data-ttu-id="d8de3-122">Описывает типы перечислений распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d8de3-122">Describes the recognizer enumeration types.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="d8de3-123">Структуры распознавателя</span><span class="sxs-lookup"><span data-stu-id="d8de3-123">Recognizer Structures</span></span>](recognizer-api-structures.md)     | <span data-ttu-id="d8de3-124">Описывает структуры распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d8de3-124">Describes the recognizer structures.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d8de3-125">Идентификаторы GUID распознавателя</span><span class="sxs-lookup"><span data-stu-id="d8de3-125">Recognizer GUIDs</span></span>](recognizer-guids.md)                   | <span data-ttu-id="d8de3-126">Указывает тип свойства для свойств пакета и свойств распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d8de3-126">Specifies the type of property for packet properties and recognizer properties.</span></span><br/>                                                                            |



 

 

 




