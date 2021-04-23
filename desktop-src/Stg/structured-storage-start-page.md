---
title: Структурированное хранилище
description: Структурированное хранилище обеспечивает сохранение файлов и данных в COM путем обработки одного файла в виде структурированной коллекции объектов, называемых хранилищами и потоками.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Структурированное хранилище Стрктд STG
- Структурированное хранилище Стрктд STG, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338236"
---
# <a name="structured-storage"></a><span data-ttu-id="8f4d3-105">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="8f4d3-105">Structured Storage</span></span>

## <a name="purpose"></a><span data-ttu-id="8f4d3-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="8f4d3-106">Purpose</span></span>

<span data-ttu-id="8f4d3-107">Структурированное хранилище обеспечивает сохранение файлов и данных в COM путем обработки одного файла в виде структурированной коллекции объектов, называемых хранилищами и потоками.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-107">Structured Storage provides file and data persistence in COM by handling a single file as a structured collection of objects known as storages and streams.</span></span>

<span data-ttu-id="8f4d3-108">Структурированное хранилище предназначено для снижения потерь производительности и издержек, связанных с хранением отдельных объектов в одном файле.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-108">The purpose of Structured Storage is to reduce the performance penalties and overhead associated with storing separate objects in a single file.</span></span> <span data-ttu-id="8f4d3-109">Структурированное хранилище предоставляет решение, определяющее способ работы с одной файловой сущностью в качестве структурированной коллекции двух типов хранилищ объектов и потоков с помощью стандартной реализации, называемой составными файлами.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-109">Structured Storage provides a solution by defining how to handle a single file entity as a structured collection of two types of objects storages and streams through a standard implementation called Compound Files.</span></span> <span data-ttu-id="8f4d3-110">Это позволяет пользователю взаимодействовать с составным файлом, а также управлять им, как если бы он был одним файлом, а не с вложенной иерархией отдельных объектов.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-110">This enables the user to interact with, and manage, a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8f4d3-111">Где применимо</span><span class="sxs-lookup"><span data-stu-id="8f4d3-111">Where applicable</span></span>

<span data-ttu-id="8f4d3-112">Структурированное хранилище можно использовать в операционных системах на основе Microsoft COM.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-112">Structured Storage can be used on Microsoft COM-based operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8f4d3-113">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="8f4d3-113">Developer audience</span></span>

<span data-ttu-id="8f4d3-114">Документация по структурированному хранилищу предназначена для опытных программистов C и C++ и разработчиков систем на основе COM.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-114">The Structured Storage documentation is intended for experienced C and C++ programmers and COM-based system developers.</span></span>

<span data-ttu-id="8f4d3-115">Структурированное хранилище в основном поддерживает языки программирования C и C++, однако любая технология на основе COM также будет поддерживать любой язык программирования, использующий указатели интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-115">Structured Storage primarily supports C and C++ programming languages, however any COM-based technology will also support any programming language that utilizes interface pointers.</span></span>

<span data-ttu-id="8f4d3-116">Глубокое понимание технологий COM является необходимым условием для разработки структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-116">A solid understanding of COM technologies is prerequisite to the developmental use of Structured Storage.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8f4d3-117">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="8f4d3-117">Run-time requirements</span></span>

<span data-ttu-id="8f4d3-118">Дополнительные сведения о том, какие операционные системы требуются для использования определенного элемента API, см. в разделе "требования" документации по элементу.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-118">For more information about which operating systems are required to use a particular API element, see the Requirements section of the documentation for the element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8f4d3-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="8f4d3-119">In this section</span></span>



| <span data-ttu-id="8f4d3-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="8f4d3-120">Topic</span></span>                                                               | <span data-ttu-id="8f4d3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8f4d3-121">Description</span></span>                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f4d3-122">Обзор</span><span class="sxs-lookup"><span data-stu-id="8f4d3-122">Overview</span></span>](about-structured-storage.md)<br/>                 | <span data-ttu-id="8f4d3-123">Общие сведения о структурированном хранилище.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-123">General information about Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="8f4d3-124">Использование структурированного хранилища</span><span class="sxs-lookup"><span data-stu-id="8f4d3-124">Using Structured Storage</span></span>](using-structured-storage.md)<br/> | <span data-ttu-id="8f4d3-125">Использование сведений для структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-125">Using information for Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8f4d3-126">Ссылки</span><span class="sxs-lookup"><span data-stu-id="8f4d3-126">Reference</span></span>](structured-storage-reference.md)<br/>            | <span data-ttu-id="8f4d3-127">Документация по интерфейсам, функциям, структурам и перечислениям структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-127">Documentation of Structured Storage specific interfaces, functions, structures, and enumerations.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="8f4d3-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="8f4d3-128">Samples</span></span>](samples.md)<br/>                                   | <span data-ttu-id="8f4d3-129">Примеры кода написаны на языке C++.</span><span class="sxs-lookup"><span data-stu-id="8f4d3-129">Code examples written in C++.</span></span> <span data-ttu-id="8f4d3-130">Дополнительные сведения см. [в разделах имена в IStorage](names-in-istorage.md), [заголовок набора свойств](property-set-header.md), [раздел](section.md), [хранение наборов свойств](storing-property-sets.md)и [Использование структурированного хранилища](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="8f4d3-130">For more information, see [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), [Storing Property Sets](storing-property-sets.md), and [Using Structured Storage](using-structured-storage.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8f4d3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8f4d3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f4d3-132">Модель COM</span><span class="sxs-lookup"><span data-stu-id="8f4d3-132">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> </dl>

 

