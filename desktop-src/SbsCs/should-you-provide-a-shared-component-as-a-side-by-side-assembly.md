---
description: Поставщики общих компонентов должны иметь возможность сделать их компонент доступным в качестве параллельной сборки, если выполняется один или несколько из следующих случаев.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Следует ли предоставлять общий компонент в качестве параллельной сборки?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912500"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a><span data-ttu-id="b2d9c-103">Следует ли предоставлять общий компонент в качестве параллельной сборки?</span><span class="sxs-lookup"><span data-stu-id="b2d9c-103">Should you provide a shared component as a side-by-side assembly?</span></span>

<span data-ttu-id="b2d9c-104">Поставщики общих компонентов должны сделать их доступными в виде параллельной сборки, если выполняется одно или несколько следующих условий.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-104">Providers of shared components should consider making their component available as a side-by-side assembly if one or more of the following are true:</span></span>

-   <span data-ttu-id="b2d9c-105">Компонент предоставляет богатый интерфейс программирования приложений, используемый многими приложениями.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-105">The component exposes a rich application programming interface that is used by many applications.</span></span> <span data-ttu-id="b2d9c-106">Например, компонент, например MSHTML, который позволяет приложениям C и C++ получать доступ к модели объектов Dynamic HTML (DHTML).</span><span class="sxs-lookup"><span data-stu-id="b2d9c-106">For example, a component such as MSHTML, which enables C and C++ applications to access the Dynamic HTML (DHTML) Object Model.</span></span>
-   <span data-ttu-id="b2d9c-107">Компонент уже является общим для нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-107">The component is already being shared by multiple applications.</span></span> <span data-ttu-id="b2d9c-108">Например, такой компонент, как COMCTL32, предоставляет приложениям доступ к общим элементам управления.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-108">For example, a component such as COMCTL32, which provides applications access to the common controls.</span></span>
-   <span data-ttu-id="b2d9c-109">Компонент является новым компонентом.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-109">The component is a new component.</span></span>
-   <span data-ttu-id="b2d9c-110">Компонент является компонентом пользовательского режима, а не драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-110">The component is a user-mode component and not a device driver.</span></span>

<span data-ttu-id="b2d9c-111">Не каждый компонент является подходящим кандидатом для параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-111">Not every component is a suitable candidate for a side-by-side assembly.</span></span> <span data-ttu-id="b2d9c-112">Компонент не является подходящим кандидатом для параллельной сборки, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-112">A component is not a suitable candidate for a side-by-side assembly if any of the following are true:</span></span>

-   <span data-ttu-id="b2d9c-113">Компонент обрабатывает взаимодействие между приложениями.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-113">The component handles communication between applications.</span></span> <span data-ttu-id="b2d9c-114">Например, части OLE32 не будут работать с хорошей параллельной сборкой, так как вы не хотите иметь две разные версии частей, которые координируют обмен данными между приложениями, запущенными в системе.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-114">For example, parts of OLE32 would not make a good side-by-side assembly because you would not want to have two different versions of the parts that coordinate communication between applications run on your system.</span></span>
-   <span data-ttu-id="b2d9c-115">Компонент управляет физическим или виртуальным устройством для системы.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-115">The component manages a physical or virtual device for the system.</span></span> <span data-ttu-id="b2d9c-116">Например, драйвер устройства для диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-116">For example a device driver for a print spooler.</span></span>

<span data-ttu-id="b2d9c-117">В некоторых случаях разработчик компонента может переконструировать существующий компонент, чтобы сделать его пригодным для публикации в качестве параллельной сборки.</span><span class="sxs-lookup"><span data-stu-id="b2d9c-117">In some cases it may be possible for the developer of the component to redesign an existing component in order to make it suitable for publication as a side-by-side assembly.</span></span> <span data-ttu-id="b2d9c-118">Дополнительные сведения см. в разделе [рекомендации по созданию параллельных сборок](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="b2d9c-118">For more information see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

 

 



