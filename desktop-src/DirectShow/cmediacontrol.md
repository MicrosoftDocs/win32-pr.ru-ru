---
description: Класс Кмедиаконтрол обеспечивает обработку базового класса для методов IDispatch сдвоенного интерфейса Имедиаконтрол. Он оставляет чисто виртуальные свойства и методы интерфейса Имедиаконтрол.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Класс Кмедиаконтрол
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914212"
---
# <a name="cmediacontrol-class"></a><span data-ttu-id="2b9d3-104">Класс Кмедиаконтрол</span><span class="sxs-lookup"><span data-stu-id="2b9d3-104">CMediaControl class</span></span>

![Иерархия классов кмедиаконтрол](images/cutil02.png)

<span data-ttu-id="2b9d3-106">`CMediaControl`Класс обеспечивает обработку базового класса для методов [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) сдвоенного интерфейса [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol).</span><span class="sxs-lookup"><span data-stu-id="2b9d3-106">The `CMediaControl` class provides base class handling of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods of the dual-interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="2b9d3-107">Он оставляет чисто виртуальные свойства и методы интерфейса **имедиаконтрол** .</span><span class="sxs-lookup"><span data-stu-id="2b9d3-107">It leaves as pure virtual the properties and methods of the **IMediaControl** interface.</span></span>

<span data-ttu-id="2b9d3-108">Как правило, диспетчер графа фильтров является единственным объектом, реализующим интерфейс [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="2b9d3-108">Typically, the filter graph manager is the only object that implements the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span> <span data-ttu-id="2b9d3-109">(фильтры реализуют интерфейс [**имедиафилтер**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , наследуемый [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), для получения управляющих команд из диспетчера графа фильтров.) Поэтому эта библиотека классов ограничена использованием для фильтрации разработчиков.</span><span class="sxs-lookup"><span data-stu-id="2b9d3-109">(filters implement the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface, inherited by [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), to receive control commands from the filter graph manager.) Therefore, this class library is of limited use to filter developers.</span></span>

<span data-ttu-id="2b9d3-110">Функции-члены [**кмедиаконтрол:: GetIdsOfNames**](cmediacontrol-getidsofnames.md), [**Кмедиаконтрол:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**Кмедиаконтрол:: Жеттипеинфокаунт**](cmediacontrol-gettypeinfocount.md)и [**кмедиаконтрол:: Invoke**](cmediacontrol-invoke.md) являются стандартными реализациями методов [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) с помощью класса [**кбаседиспатч**](cbasedispatch.md) (и библиотеки типов) для анализа команд и передачи их в чистые виртуальные методы интерфейса [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="2b9d3-110">The [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md), and [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member functions are standard implementations of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span>

<span data-ttu-id="2b9d3-111">Методы [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) , определенные в Control. ODL, остаются нечистыми виртуальными.</span><span class="sxs-lookup"><span data-stu-id="2b9d3-111">The [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods, defined in control.odl, are left as pure virtual.</span></span>



| <span data-ttu-id="2b9d3-112">Функции элементов</span><span class="sxs-lookup"><span data-stu-id="2b9d3-112">Member Functions</span></span>                                           | <span data-ttu-id="2b9d3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2b9d3-113">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b9d3-114">**кмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="2b9d3-114">**CMediaControl**</span></span>](cmediacontrol-cmediacontrol.md)       | <span data-ttu-id="2b9d3-115">Конструирует объект **кмедиаконтрол** .</span><span class="sxs-lookup"><span data-stu-id="2b9d3-115">Constructs a **CMediaControl** object.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="2b9d3-116">Методы IDispatch</span><span class="sxs-lookup"><span data-stu-id="2b9d3-116">IDispatch Methods</span></span>                                          | <span data-ttu-id="2b9d3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2b9d3-117">Description</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="2b9d3-118">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="2b9d3-118">**GetIDsOfNames**</span></span>](cmediacontrol-getidsofnames.md)       | <span data-ttu-id="2b9d3-119">Сопоставляет один элемент и необязательный набор параметров с соответствующим набором целочисленных идентификаторов диспетчеризации (DISPID), которые могут использоваться при последующих вызовах метода [**кмедиаконтрол:: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="2b9d3-119">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used during subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) method.</span></span> |
| [<span data-ttu-id="2b9d3-120">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="2b9d3-120">**GetTypeInfo**</span></span>](cmediacontrol-gettypeinfo.md)           | <span data-ttu-id="2b9d3-121">Извлекает объект сведений о типе, который может получить сведения о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b9d3-121">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>                                                                                                                                          |
| [<span data-ttu-id="2b9d3-122">**жеттипеинфокаунт**</span><span class="sxs-lookup"><span data-stu-id="2b9d3-122">**GetTypeInfoCount**</span></span>](cmediacontrol-gettypeinfocount.md) | <span data-ttu-id="2b9d3-123">Извлекает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="2b9d3-123">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="2b9d3-124">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="2b9d3-124">**Invoke**</span></span>](cmediacontrol-invoke.md)                     | <span data-ttu-id="2b9d3-125">Предоставляет доступ к открытым свойствам и методам объекта.</span><span class="sxs-lookup"><span data-stu-id="2b9d3-125">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                                                                         |



 

 

 
