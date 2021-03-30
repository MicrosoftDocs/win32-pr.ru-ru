---
description: Класс Кмедиаевент предоставляет реализацию базового класса для методов IDispatch сдвоенного интерфейса Имедиаевент. Он оставляет чисто виртуальные свойства и методы интерфейса Имедиаевент.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Класс Кмедиаевент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273288"
---
# <a name="cmediaevent-class"></a><span data-ttu-id="a1108-104">Класс Кмедиаевент</span><span class="sxs-lookup"><span data-stu-id="a1108-104">CMediaEvent class</span></span>

![Иерархия классов кмедиаевент](images/cutil03.png)

<span data-ttu-id="a1108-106">`CMediaEvent`Класс предоставляет реализацию базового класса для методов **IDispatch** сдвоенного интерфейса [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent).</span><span class="sxs-lookup"><span data-stu-id="a1108-106">The `CMediaEvent` class provides base class implementation of the **IDispatch** methods of the dual-interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span> <span data-ttu-id="a1108-107">Он оставляет чисто виртуальные свойства и методы интерфейса **имедиаевент** .</span><span class="sxs-lookup"><span data-stu-id="a1108-107">It leaves as pure virtual the properties and methods of the **IMediaEvent** interface.</span></span>

<span data-ttu-id="a1108-108">`CMediaEvent`Класс также предоставляет реализацию базового класса интерфейса [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) , производного от [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent).</span><span class="sxs-lookup"><span data-stu-id="a1108-108">The `CMediaEvent` class also provides base class implementation of the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface which derives from [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span>

<span data-ttu-id="a1108-109">Функции-члены [**кмедиаевент:: GetIdsOfNames**](cmediaevent-getidsofnames.md), [**Кмедиаевент:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**Кмедиаевент:: Жеттипеинфокаунт**](cmediaevent-gettypeinfocount.md)и [**кмедиаевент:: Invoke**](cmediaevent-invoke.md) являются стандартными реализациями интерфейса **IDispatch** с помощью класса [**кбаседиспатч**](cbasedispatch.md) (и библиотеки типов) для анализа команд и передачи их в чистые виртуальные методы интерфейса [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="a1108-109">The [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md), and [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member functions are standard implementations of the **IDispatch** interface using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>



| <span data-ttu-id="a1108-110">Функции элементов</span><span class="sxs-lookup"><span data-stu-id="a1108-110">Member Functions</span></span>                                         | <span data-ttu-id="a1108-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a1108-111">Description</span></span>                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1108-112">**кмедиаевент**</span><span class="sxs-lookup"><span data-stu-id="a1108-112">**CMediaEvent**</span></span>](cmediaevent-cmediaevent.md)           | <span data-ttu-id="a1108-113">Конструирует объект **кмедиаевент** .</span><span class="sxs-lookup"><span data-stu-id="a1108-113">Constructs a **CMediaEvent** object.</span></span>                                                                                                                                                          |
| <span data-ttu-id="a1108-114">Методы IDispatch</span><span class="sxs-lookup"><span data-stu-id="a1108-114">IDispatch Methods</span></span>                                        | <span data-ttu-id="a1108-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a1108-115">Description</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="a1108-116">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="a1108-116">**GetIDsOfNames**</span></span>](cmediaevent-getidsofnames.md)       | <span data-ttu-id="a1108-117">Сопоставляет один элемент и необязательный набор параметров с соответствующим набором целочисленных идентификаторов диспетчеризации, которые могут использоваться при последующих вызовах метода **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="a1108-117">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used during subsequent calls to the **IDispatch::Invoke** method.</span></span> |
| [<span data-ttu-id="a1108-118">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="a1108-118">**GetTypeInfo**</span></span>](cmediaevent-gettypeinfo.md)           | <span data-ttu-id="a1108-119">Извлекает объект сведений о типе, который извлекает сведения о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a1108-119">Retrieves a type-information object, which retrieves the type information for an interface.</span></span>                                                                                                   |
| [<span data-ttu-id="a1108-120">**жеттипеинфокаунт**</span><span class="sxs-lookup"><span data-stu-id="a1108-120">**GetTypeInfoCount**</span></span>](cmediaevent-gettypeinfocount.md) | <span data-ttu-id="a1108-121">Извлекает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="a1108-121">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                    |
| [<span data-ttu-id="a1108-122">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="a1108-122">**Invoke**</span></span>](cmediaevent-invoke.md)                     | <span data-ttu-id="a1108-123">Предоставляет доступ к открытым свойствам и методам объекта.</span><span class="sxs-lookup"><span data-stu-id="a1108-123">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                               |



 

 

 



