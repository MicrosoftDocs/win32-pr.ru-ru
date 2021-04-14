---
title: Классы, объекты и интерфейсы
description: Классы, объекты и интерфейсы
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104488505"
---
# <a name="classes-objects-and-interfaces"></a><span data-ttu-id="72b74-103">Классы, объекты и интерфейсы</span><span class="sxs-lookup"><span data-stu-id="72b74-103">Classes, Objects, and Interfaces</span></span>

<span data-ttu-id="72b74-104">В языке программирования C++ *класс* состоит из *свойств* (или данных элемента) и *методов* (или функций-членов).</span><span class="sxs-lookup"><span data-stu-id="72b74-104">In the C++ programming language, a *class* consists of *properties* (or member data) and *methods* (or member functions).</span></span> <span data-ttu-id="72b74-105">Свойства — это элементы данных, например содержащиеся в структуре.</span><span class="sxs-lookup"><span data-stu-id="72b74-105">The properties are data elements, such as those contained in a structure.</span></span> <span data-ttu-id="72b74-106">Методы используются для различных целей, таких как инициализация, назначение, операции и доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="72b74-106">The methods are used for a variety of purposes, such as initialization, assignment, operations, and data access.</span></span> <span data-ttu-id="72b74-107">Объявление класса используется так же, как и объявление структуры.</span><span class="sxs-lookup"><span data-stu-id="72b74-107">You use a class declaration in the same way that you use a structure declaration.</span></span> <span data-ttu-id="72b74-108">Память выделяется для класса при определении *объекта* класса.</span><span class="sxs-lookup"><span data-stu-id="72b74-108">Memory is allocated for a class when you define a class *object*.</span></span> <span data-ttu-id="72b74-109">Каждый объект класса имеет область данных для своих свойств и таблицу указателей на поддерживаемые методы.</span><span class="sxs-lookup"><span data-stu-id="72b74-109">Each class object has a data area for its properties and a table of pointers to the methods it supports.</span></span>

<span data-ttu-id="72b74-110">В OLE объект состоит из данных и методов, как это делается в C++.</span><span class="sxs-lookup"><span data-stu-id="72b74-110">In OLE, an object consists of data and methods, as it does in C++.</span></span> <span data-ttu-id="72b74-111">Однако объект OLE соответствует более строгому правилу.</span><span class="sxs-lookup"><span data-stu-id="72b74-111">However, an OLE object adheres to stricter rules.</span></span> <span data-ttu-id="72b74-112">Данные являются строго внутренними.</span><span class="sxs-lookup"><span data-stu-id="72b74-112">The data is strictly internal.</span></span> <span data-ttu-id="72b74-113">Объект предоставляет только интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="72b74-113">An object only exposes interfaces.</span></span> <span data-ttu-id="72b74-114">*Интерфейс* — это набор связанных методов для объекта.</span><span class="sxs-lookup"><span data-stu-id="72b74-114">An *interface* is a set of related methods for an object.</span></span> <span data-ttu-id="72b74-115">Каждый объект может поддерживать несколько интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="72b74-115">Each object can support multiple interfaces.</span></span> <span data-ttu-id="72b74-116">Все интерфейсы OLE поддерживают интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="72b74-116">All OLE interfaces support the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

 

 




