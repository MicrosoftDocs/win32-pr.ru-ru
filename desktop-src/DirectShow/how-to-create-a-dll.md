---
description: Создание библиотеки DLL фильтра DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Создание библиотеки DLL фильтра DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650412"
---
# <a name="how-to-create-a-directshow-filter-dll"></a><span data-ttu-id="7c1c8-103">Создание библиотеки DLL фильтра DirectShow</span><span class="sxs-lookup"><span data-stu-id="7c1c8-103">How to Create a DirectShow Filter DLL</span></span>

<span data-ttu-id="7c1c8-104">В этой статье описывается, как реализовать компонент в виде библиотеки динамической компоновки (DLL) в Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7c1c8-104">This article describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span> <span data-ttu-id="7c1c8-105">Эта статья является продолжением [реализации IUnknown](how-to-implement-iunknown.md), который описывает, как реализовать интерфейс **IUnknown** путем наследования компонента от базового класса [**кункновн**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1c8-105">This article is a continuation from [How to Implement IUnknown](how-to-implement-iunknown.md), which describes how to implement the **IUnknown** interface by deriving your component from the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="7c1c8-106">Эта статья состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="7c1c8-106">This article contains the following sections.</span></span>

-   [<span data-ttu-id="7c1c8-107">Фабрики классов и шаблоны фабрики</span><span class="sxs-lookup"><span data-stu-id="7c1c8-107">Class Factories and Factory Templates</span></span>](class-factories-and-factory-templates.md)
-   [<span data-ttu-id="7c1c8-108">Массив шаблонов фабрики</span><span class="sxs-lookup"><span data-stu-id="7c1c8-108">Factory Template Array</span></span>](factory-template-array.md)
-   [<span data-ttu-id="7c1c8-109">Функции DLL</span><span class="sxs-lookup"><span data-stu-id="7c1c8-109">DLL Functions</span></span>](dll-functions.md)

<span data-ttu-id="7c1c8-110">Для регистрации фильтра DirectShow (в отличие от универсального COM-объекта) требуются некоторые дополнительные действия, не описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="7c1c8-110">Registering a DirectShow filter (as opposed to a generic COM object) requires some additional steps that are not covered in this article.</span></span> <span data-ttu-id="7c1c8-111">Сведения о регистрации фильтров см. [в статье регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7c1c8-111">For information on registering filters, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c1c8-112">См. также</span><span class="sxs-lookup"><span data-stu-id="7c1c8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c1c8-113">DirectShow и COM</span><span class="sxs-lookup"><span data-stu-id="7c1c8-113">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



