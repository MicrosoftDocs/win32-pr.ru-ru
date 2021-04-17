---
title: Объект Error (пакет SDK для WMP)
description: Объект Error предоставляет доступ к коллекции объектов Ерроритем.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Проигрыватель Windows Media Object Error
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2019
ms.locfileid: "105691426"
---
# <a name="error-object"></a><span data-ttu-id="2b5ed-104">Объект Error</span><span class="sxs-lookup"><span data-stu-id="2b5ed-104">Error Object</span></span>

<span data-ttu-id="2b5ed-105">Объект **Error** предоставляет доступ к коллекции объектов [ерроритем](erroritem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="2b5ed-105">The **Error** object provides access to a collection of [ErrorItem](erroritem-object.md) objects.</span></span>

<span data-ttu-id="2b5ed-106">Объект **Error** поддерживает следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="2b5ed-106">The **Error** object supports the following property.</span></span>



| <span data-ttu-id="2b5ed-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="2b5ed-107">Property</span></span>                           | <span data-ttu-id="2b5ed-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2b5ed-108">Description</span></span>                                        |
|------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2b5ed-109">ерроркаунт</span><span class="sxs-lookup"><span data-stu-id="2b5ed-109">errorCount</span></span>](error-errorcount.md) | <span data-ttu-id="2b5ed-110">Возвращает количество ошибок в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="2b5ed-110">Retrieves the number of errors in the error queue.</span></span> |



 

<span data-ttu-id="2b5ed-111">Объект **Error** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2b5ed-111">The **Error** object supports the following methods.</span></span>



| <span data-ttu-id="2b5ed-112">Метод</span><span class="sxs-lookup"><span data-stu-id="2b5ed-112">Method</span></span>                                       | <span data-ttu-id="2b5ed-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2b5ed-113">Description</span></span>                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b5ed-114">клеарерроркуеуе</span><span class="sxs-lookup"><span data-stu-id="2b5ed-114">clearErrorQueue</span></span>](error-clearerrorqueue.md) | <span data-ttu-id="2b5ed-115">Удаляет ошибки из очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="2b5ed-115">Clears the errors from the error queue.</span></span>                                                         |
| [<span data-ttu-id="2b5ed-116">Item</span><span class="sxs-lookup"><span data-stu-id="2b5ed-116">item</span></span>](error-item.md)                       | <span data-ttu-id="2b5ed-117">Извлекает объект [ерроритем](erroritem-object.md) из очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="2b5ed-117">Retrieves an [ErrorItem](erroritem-object.md) object from the error queue.</span></span>                     |
| [<span data-ttu-id="2b5ed-118">Справка</span><span class="sxs-lookup"><span data-stu-id="2b5ed-118">webHelp</span></span>](error-webhelp.md)                 | <span data-ttu-id="2b5ed-119">Открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2b5ed-119">Launches the Windows Media Player Web Help page to display further information about the error.</span></span> |



 

<span data-ttu-id="2b5ed-120">Доступ к объекту **Error** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="2b5ed-120">The **Error** object is accessed through the following property.</span></span>



| <span data-ttu-id="2b5ed-121">Объект</span><span class="sxs-lookup"><span data-stu-id="2b5ed-121">Object</span></span>                      | <span data-ttu-id="2b5ed-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="2b5ed-122">Property</span></span>                  |
|-----------------------------|---------------------------|
| [<span data-ttu-id="2b5ed-123">Игрок</span><span class="sxs-lookup"><span data-stu-id="2b5ed-123">Player</span></span>](player-object.md) | [<span data-ttu-id="2b5ed-124">error</span><span class="sxs-lookup"><span data-stu-id="2b5ed-124">error</span></span>](player-error.md) |



 

## <a name="see-also"></a><span data-ttu-id="2b5ed-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b5ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5ed-126">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="2b5ed-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




