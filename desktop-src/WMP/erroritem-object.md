---
title: Объект Ерроритем
description: Объект Ерроритем предоставляет способ доступа к сведениям об ошибках.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Проигрыватель Windows Media Object Ерроритем
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105691410"
---
# <a name="erroritem-object"></a><span data-ttu-id="6d711-104">Объект Ерроритем</span><span class="sxs-lookup"><span data-stu-id="6d711-104">ErrorItem Object</span></span>

<span data-ttu-id="6d711-105">Объект **ерроритем** предоставляет способ доступа к сведениям об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6d711-105">The **ErrorItem** object provides a way to access error information.</span></span>

<span data-ttu-id="6d711-106">Объект **ерроритем** поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="6d711-106">The **ErrorItem** object supports the following properties.</span></span>



| <span data-ttu-id="6d711-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="6d711-107">Property</span></span>                                           | <span data-ttu-id="6d711-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6d711-108">Description</span></span>                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d711-109">выполняет</span><span class="sxs-lookup"><span data-stu-id="6d711-109">condition</span></span>](erroritem-condition.md)               | <span data-ttu-id="6d711-110">Извлекает значение, указывающее условие для ошибки.</span><span class="sxs-lookup"><span data-stu-id="6d711-110">Retrieves a value indicating the condition for the error.</span></span>                                       |
| [<span data-ttu-id="6d711-111">кустомурл</span><span class="sxs-lookup"><span data-stu-id="6d711-111">customUrl</span></span>](erroritem-customurl.md)               | <span data-ttu-id="6d711-112">Извлекает URL-адрес сайта, который отображает конкретные сведения о сбое загрузки кодека.</span><span class="sxs-lookup"><span data-stu-id="6d711-112">Retrieves the URL of a website that displays specific information about codec download failure.</span></span> |
| [<span data-ttu-id="6d711-113">errorCode</span><span class="sxs-lookup"><span data-stu-id="6d711-113">errorCode</span></span>](erroritem-errorcode.md)               | <span data-ttu-id="6d711-114">Извлекает текущий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6d711-114">Retrieves the current error code.</span></span>                                                               |
| [<span data-ttu-id="6d711-115">еррорконтекст</span><span class="sxs-lookup"><span data-stu-id="6d711-115">errorContext</span></span>](erroritem-errorcontext.md)         | <span data-ttu-id="6d711-116">Извлекает значение, указывающее контекст ошибки.</span><span class="sxs-lookup"><span data-stu-id="6d711-116">Retrieves a value indicating the context of the error.</span></span>                                          |
| [<span data-ttu-id="6d711-117">errorDescription</span><span class="sxs-lookup"><span data-stu-id="6d711-117">errorDescription</span></span>](erroritem-errordescription.md) | <span data-ttu-id="6d711-118">Извлекает описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="6d711-118">Retrieves a description of the error.</span></span>                                                           |
| <span data-ttu-id="6d711-119">**исправить**</span><span class="sxs-lookup"><span data-stu-id="6d711-119">**remedy**</span></span>                                         | <span data-ttu-id="6d711-120">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="6d711-120">Reserved for future use.</span></span>                                                                        |



 

<span data-ttu-id="6d711-121">Доступ к объекту **ерроритем** осуществляется с помощью следующих методов.</span><span class="sxs-lookup"><span data-stu-id="6d711-121">The **ErrorItem** object is accessed through the following methods.</span></span>



| <span data-ttu-id="6d711-122">Объект</span><span class="sxs-lookup"><span data-stu-id="6d711-122">Object</span></span>                    | <span data-ttu-id="6d711-123">Метод</span><span class="sxs-lookup"><span data-stu-id="6d711-123">Method</span></span>                   |
|---------------------------|--------------------------|
| [<span data-ttu-id="6d711-124">Ошибка</span><span class="sxs-lookup"><span data-stu-id="6d711-124">Error</span></span>](error-object.md) | [<span data-ttu-id="6d711-125">Item</span><span class="sxs-lookup"><span data-stu-id="6d711-125">item</span></span>](error-item.md)   |
| [<span data-ttu-id="6d711-126">Носитель</span><span class="sxs-lookup"><span data-stu-id="6d711-126">Media</span></span>](media-object.md) | [<span data-ttu-id="6d711-127">error</span><span class="sxs-lookup"><span data-stu-id="6d711-127">error</span></span>](media-error.md) |



 

<span data-ttu-id="6d711-128">В целях иллюстрации, *Player*. *Ошибка*. *элемент*(*индекс*) используется в разделах синтаксиса Reference.</span><span class="sxs-lookup"><span data-stu-id="6d711-128">For purposes of illustration, *player*.*error*.*item*(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d711-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d711-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d711-130">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="6d711-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




