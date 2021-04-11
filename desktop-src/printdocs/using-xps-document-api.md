---
description: В этом разделе описывается использование API документа XPS для выполнения задач программирования.
ms.assetid: 05b3d7b6-7628-4a5f-87b7-9d51ead51c79
title: Использование API документов XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8870c64bfa8fe478fb71174703c82a96e3723c53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999348"
---
# <a name="using-xps-document-api"></a><span data-ttu-id="1ec02-103">Использование API документов XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-103">Using XPS Document API</span></span>

<span data-ttu-id="1ec02-104">В этом разделе описывается использование [API документа XPS](documents-xps.md) для выполнения задач программирования.</span><span class="sxs-lookup"><span data-stu-id="1ec02-104">This section describes how to use the [XPS Document API](documents-xps.md) to perform programming tasks.</span></span>

<span data-ttu-id="1ec02-105">Примеры использования [API документов XPS](documents-xps.md) в программе см. в разделе [задачи программирования API документов XPS](#xps-document-api-programming-tasks) .</span><span class="sxs-lookup"><span data-stu-id="1ec02-105">For examples of how to use the [XPS Document API](documents-xps.md) in a program, see the [XPS Document API Programming Tasks](#xps-document-api-programming-tasks) section.</span></span>

<span data-ttu-id="1ec02-106">Сведения о том, как использовать объектную модель XPS и как она реализована с помощью [API документов XPS](documents-xps.md), см. в статье [об API документов XPS](about-xps-document-api.md).</span><span class="sxs-lookup"><span data-stu-id="1ec02-106">For information about how to use the XPS Object Model and how it is implemented by the [XPS Document API](documents-xps.md), see [About XPS Document API](about-xps-document-api.md).</span></span>

## <a name="getting-started-with-the-xps-document-api"></a><span data-ttu-id="1ec02-107">начало работы с помощью API документа XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-107">Getting Started with the XPS Document API</span></span>

<span data-ttu-id="1ec02-108">Прежде чем приступить к работе с API документов XPS, ознакомьтесь со следующими разделами по программированию:</span><span class="sxs-lookup"><span data-stu-id="1ec02-108">Before you start using the XPS Document API, make sure that you are familiar with the following programming topics:</span></span><dl>

[<span data-ttu-id="1ec02-109">Программирование COM</span><span class="sxs-lookup"><span data-stu-id="1ec02-109">COM Programming</span></span>](/windows/desktop/com/component-object-model--com--portal)  
[<span data-ttu-id="1ec02-110">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="1ec02-110">Error Handling in COM</span></span>](/windows/desktop/com/error-handling-in-com)  
</dl>

<span data-ttu-id="1ec02-111">При использовании API документов XPS может также потребоваться использовать следующие технологии:</span><span class="sxs-lookup"><span data-stu-id="1ec02-111">When using the XPS Document API, you might also want to use the following technologies:</span></span><dl>

[<span data-ttu-id="1ec02-112">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="1ec02-112">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)  
[<span data-ttu-id="1ec02-113">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-113">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)  
[<span data-ttu-id="1ec02-114">API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-114">XPS Digital Signature API</span></span>](xps-digital-signatures.md)  
</dl>

## <a name="xps-document-api-programming-tasks"></a><span data-ttu-id="1ec02-115">Задачи программирования API документов XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-115">XPS Document API Programming Tasks</span></span>

<span data-ttu-id="1ec02-116">В подразделах этого раздела описывается использование [API документов XPS](documents-xps.md) в программе и демонстрация выполнения некоторых распространенных задач программирования.</span><span class="sxs-lookup"><span data-stu-id="1ec02-116">The topics in this section describe how to use the [XPS Document API](documents-xps.md) in a program and demonstrate how to perform some common programming tasks.</span></span>

<span data-ttu-id="1ec02-117">API документа XPS использует коллекции для работы с группами интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="1ec02-117">The XPS Document API uses collections to work with groups of interfaces.</span></span> <span data-ttu-id="1ec02-118">[Работа с интерфейсами коллекции Operations Manager XPS](working-with-xps-object-model-collection-interfaces.md) описывает, как программировать с помощью этих коллекций.</span><span class="sxs-lookup"><span data-stu-id="1ec02-118">[Working with XPS OM Collection Interfaces](working-with-xps-object-model-collection-interfaces.md) describes how to program with these collections.</span></span>

<span data-ttu-id="1ec02-119">Ниже перечислены [распространенные задачи программирования документов XPS](common-xps-document-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec02-119">The [Common XPS Document Programming Tasks](common-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="1ec02-120">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-120">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="1ec02-121">Создание пустой объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-121">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="1ec02-122">Чтение XPS-документа в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-122">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="1ec02-123">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-123">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="1ec02-124">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-124">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="1ec02-125">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-125">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="1ec02-126">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-126">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="1ec02-127">Запись объектной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-127">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="1ec02-128">Печать OM-объекта XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-128">Print an XPS OM</span></span>](print-an-xps-om.md)  
  
</dl>

<span data-ttu-id="1ec02-129">К [дополнительным задачам программирования документов XPS](advanced-xps-document-tasks.md) относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="1ec02-129">The [Advanced XPS Document Programming Tasks](advanced-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="1ec02-130">Слияние XPS-документов</span><span class="sxs-lookup"><span data-stu-id="1ec02-130">Merge XPS Documents</span></span>](merging-xps-documents.md)  
[<span data-ttu-id="1ec02-131">Обработка документов XPS в фильтре XPSDrv</span><span class="sxs-lookup"><span data-stu-id="1ec02-131">Processing XPS Documents in an XPSDrv Filter</span></span>](processing-xps-documents-in-an-xpsdrv-filter.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="1ec02-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1ec02-132">Related topics</span></span>

<dl> <span data-ttu-id="1ec02-133"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1ec02-133"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1ec02-134">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-134">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="1ec02-135">XPS</span><span class="sxs-lookup"><span data-stu-id="1ec02-135">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
