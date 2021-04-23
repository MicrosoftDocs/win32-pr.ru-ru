---
title: Приступая к разработке пользовательского интерфейса для приложений Windows
description: .
ms.assetid: 29d6f67b-46fa-4f39-a319-306c832eff9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c3d1a182aef6354901f0fa71f94b39ecdc58f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792984"
---
# <a name="getting-started-developing-user-interfaces-for-windows-applications"></a><span data-ttu-id="d8e03-103">начало работы разработке пользовательских интерфейсов для приложений Windows</span><span class="sxs-lookup"><span data-stu-id="d8e03-103">Getting Started Developing User Interfaces for Windows Applications</span></span>

## <a name="purpose"></a><span data-ttu-id="d8e03-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="d8e03-104">Purpose</span></span>

<span data-ttu-id="d8e03-105">Следующие разделы содержат общие рекомендации для разработчиков, которые разрабатывают, реализуют и тестируют пользовательский интерфейс приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="d8e03-105">The following sections offer general guidance to developers who are designing, implementing, and testing the user interface of a Windows application.</span></span>

<span data-ttu-id="d8e03-106">В дополнение к основным принципам разработки пользовательских интерфейсов предоставляется множество рекомендаций и предложений, которые помогут разработчикам обеспечить простоту, эффективность и удобство работы пользователей.</span><span class="sxs-lookup"><span data-stu-id="d8e03-106">In addition to basic user interface design principles, numerous recommendations and suggestions are provided that will help developers provide a user experience that is as simple, efficient, and enjoyable as possible.</span></span>

> [!Note]  
> <span data-ttu-id="d8e03-107">Эти рекомендации не должны быть исчерпывающими и подчиняются определенной области и функциональности приложения.</span><span class="sxs-lookup"><span data-stu-id="d8e03-107">These guidelines are not intended to be comprehensive and are subject to the specific scope and functionality of an application.</span></span> <span data-ttu-id="d8e03-108">Более подробные инструкции см. в руководстве по взаимодействию с [пользователем Windows](../uxguide/guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="d8e03-108">For more comprehensive guidelines, see the [Windows User Experience Interaction Guidelines](../uxguide/guidelines.md).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="d8e03-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d8e03-109">In this section</span></span>



| <span data-ttu-id="d8e03-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="d8e03-110">Topic</span></span>                                                                            | <span data-ttu-id="d8e03-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d8e03-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8e03-112">Общие сведения о процессе разработки пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d8e03-112">Overview of the User Interface Development Process</span></span>](the-process.md)<br/> | <span data-ttu-id="d8e03-113">В этом разделе описываются три этапа проектирования пользовательского интерфейса и приводятся задачи, которые обычно связаны с каждым этапом.</span><span class="sxs-lookup"><span data-stu-id="d8e03-113">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span><br/>                                              |
| [<span data-ttu-id="d8e03-114">Проектирование пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d8e03-114">Designing a User Interface</span></span>](designing-a-user-interface.md)<br/>          | <span data-ttu-id="d8e03-115">В этом разделе подробно описаны некоторые задачи, связанные с проектированием пользовательского интерфейса для приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="d8e03-115">This section describes in detail some of the tasks associated with designing a UI for a Windows application.</span></span><br/>                                                                         |
| [<span data-ttu-id="d8e03-116">Реализация пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d8e03-116">Implementing a User Interface</span></span>](implementing-a-user-interface.md)<br/>    | <span data-ttu-id="d8e03-117">В этом разделе описываются некоторые задачи, связанные с реализацией пользовательского интерфейса для приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="d8e03-117">This section describes some of the tasks associated with implementing a user interface for a Windows application.</span></span><br/>                                                                    |
| [<span data-ttu-id="d8e03-118">Тестирование пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d8e03-118">Testing a User Interface</span></span>](testing-a-user-interface.md)<br/>              | <span data-ttu-id="d8e03-119">В этом разделе подробно описаны некоторые задачи, связанные с тестированием пользовательского интерфейса для приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="d8e03-119">This section describes in detail some of the tasks associated with testing a UI for a Windows application.</span></span><br/>                                                                           |
| [<span data-ttu-id="d8e03-120">Вопросы безопасности: Пользовательский интерфейс Windows</span><span class="sxs-lookup"><span data-stu-id="d8e03-120">Security Considerations: Windows User Interface</span></span>](sec-ui.md)<br/>         | <span data-ttu-id="d8e03-121">В этом разделе содержатся сведения о вопросах безопасности в пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="d8e03-121">This topic provides information about security considerations in the Windows User Interface.</span></span><br/>                                                                                         |
| [<span data-ttu-id="d8e03-122">Другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="d8e03-122">Other Resources</span></span>](other-resources.md)<br/>                                | <span data-ttu-id="d8e03-123">Этот раздел содержит список рекомендуемых книг и ресурсов, связанных с проектированием пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d8e03-123">This section contains a list of recommended books and resources related to user interface design.</span></span> <span data-ttu-id="d8e03-124">(Эти книги и ресурсы могут быть недоступны в некоторых языках и странах.)</span><span class="sxs-lookup"><span data-stu-id="d8e03-124">(These books and resources may not be available in some languages and countries.)</span></span> <br/> |



 

 

