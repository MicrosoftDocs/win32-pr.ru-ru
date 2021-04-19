---
description: Интерфейс Иамтимелинетрансабле добавляет переходы к объекту в службах редактирования DirectShow (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Интерфейс Иамтимелинетрансабле (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689411"
---
# <a name="iamtimelinetransable-interface"></a><span data-ttu-id="967ab-103">Интерфейс Иамтимелинетрансабле</span><span class="sxs-lookup"><span data-stu-id="967ab-103">IAMTimelineTransable interface</span></span>

> [!Note]  
> <span data-ttu-id="967ab-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="967ab-104">\[Deprecated.</span></span> <span data-ttu-id="967ab-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="967ab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="967ab-106">`IAMTimelineTransable`Интерфейс добавляет переходы к объекту в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="967ab-106">The `IAMTimelineTransable` interface adds transitions to an object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="967ab-107">Этот интерфейс предоставляется любым объектом, к которому могут применяться переходы, включая записи, композиции и группы.</span><span class="sxs-lookup"><span data-stu-id="967ab-107">This interface is exposed by any object that can have transitions applied to it, including tracks, compositions, and groups.</span></span> <span data-ttu-id="967ab-108">Объект, реализующий этот интерфейс, может иметь любое количество переходов, но переходы не должны перекрываться по времени.</span><span class="sxs-lookup"><span data-stu-id="967ab-108">An object that implements this interface can have any number of transitions, but the transitions must not overlap in time.</span></span>

> [!Note]  
> <span data-ttu-id="967ab-109">Звук не поддерживает переходы.</span><span class="sxs-lookup"><span data-stu-id="967ab-109">Audio does not support transitions.</span></span> <span data-ttu-id="967ab-110">Объекты внутри звуковых групп могут предоставлять `IAMTimelineTransable` интерфейс, но приложение не должно добавлять к ним переходы.</span><span class="sxs-lookup"><span data-stu-id="967ab-110">Objects within audio groups can expose the `IAMTimelineTransable` interface, but the application should not add transitions to them.</span></span>

 

## <a name="members"></a><span data-ttu-id="967ab-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="967ab-111">Members</span></span>

<span data-ttu-id="967ab-112">Интерфейс **иамтимелинетрансабле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="967ab-112">The **IAMTimelineTransable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="967ab-113">**Иамтимелинетрансабле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="967ab-113">**IAMTimelineTransable** also has these types of members:</span></span>

-   [<span data-ttu-id="967ab-114">Методы</span><span class="sxs-lookup"><span data-stu-id="967ab-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="967ab-115">Методы</span><span class="sxs-lookup"><span data-stu-id="967ab-115">Methods</span></span>

<span data-ttu-id="967ab-116">Интерфейс **иамтимелинетрансабле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="967ab-116">The **IAMTimelineTransable** interface has these methods.</span></span>



| <span data-ttu-id="967ab-117">Метод</span><span class="sxs-lookup"><span data-stu-id="967ab-117">Method</span></span>                                                          | <span data-ttu-id="967ab-118">Описание</span><span class="sxs-lookup"><span data-stu-id="967ab-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="967ab-119">**жетнексттранс**</span><span class="sxs-lookup"><span data-stu-id="967ab-119">**GetNextTrans**</span></span>](iamtimelinetransable-getnexttrans.md)       | <span data-ttu-id="967ab-120">Извлекает первый переход, который отображается в указанное время или позже.</span><span class="sxs-lookup"><span data-stu-id="967ab-120">Retrieves the first transition that appears at the specified time or later.</span></span><br/>                                             |
| [<span data-ttu-id="967ab-121">**GetNextTrans2**</span><span class="sxs-lookup"><span data-stu-id="967ab-121">**GetNextTrans2**</span></span>](iamtimelinetransable-getnexttrans2.md)     | <span data-ttu-id="967ab-122">Извлекает первый переход, который отображается в указанное время или более поздней версии, с временем, указанным в качестве значения **рефтиме** .</span><span class="sxs-lookup"><span data-stu-id="967ab-122">Retrieves the first transition that appears at the specified time or later, with the time given as a **REFTIME** value.</span></span><br/> |
| [<span data-ttu-id="967ab-123">**жеттрансаттиме**</span><span class="sxs-lookup"><span data-stu-id="967ab-123">**GetTransAtTime**</span></span>](iamtimelinetransable-gettransattime.md)   | <span data-ttu-id="967ab-124">Извлекает переход, ближайший к указанному времени.</span><span class="sxs-lookup"><span data-stu-id="967ab-124">Retrieves the transition nearest to the specified time.</span></span><br/>                                                                 |
| [<span data-ttu-id="967ab-125">**GetTransAtTime2**</span><span class="sxs-lookup"><span data-stu-id="967ab-125">**GetTransAtTime2**</span></span>](iamtimelinetransable-gettransattime2.md) | <span data-ttu-id="967ab-126">Получает ближайшее к указанному времени переход, заданный как значение **рефтиме** .</span><span class="sxs-lookup"><span data-stu-id="967ab-126">Retrieves the transition nearest to the specified time, given as a **REFTIME** value.</span></span><br/>                                   |
| [<span data-ttu-id="967ab-127">**трансадд**</span><span class="sxs-lookup"><span data-stu-id="967ab-127">**TransAdd**</span></span>](iamtimelinetransable-transadd.md)               | <span data-ttu-id="967ab-128">Добавляет переход к объекту.</span><span class="sxs-lookup"><span data-stu-id="967ab-128">Adds a transition to the object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="967ab-129">**трансжеткаунт**</span><span class="sxs-lookup"><span data-stu-id="967ab-129">**TransGetCount**</span></span>](iamtimelinetransable-transgetcount.md)     | <span data-ttu-id="967ab-130">Возвращает число переходов для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="967ab-130">Retrieves the number of transitions on this object.</span></span><br/>                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="967ab-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="967ab-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="967ab-132">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="967ab-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="967ab-133">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="967ab-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="967ab-134">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="967ab-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="967ab-135">Требования</span><span class="sxs-lookup"><span data-stu-id="967ab-135">Requirements</span></span>



| <span data-ttu-id="967ab-136">Требование</span><span class="sxs-lookup"><span data-stu-id="967ab-136">Requirement</span></span> | <span data-ttu-id="967ab-137">Значение</span><span class="sxs-lookup"><span data-stu-id="967ab-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="967ab-138">Header</span><span class="sxs-lookup"><span data-stu-id="967ab-138">Header</span></span><br/>  | <dl> <span data-ttu-id="967ab-139"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="967ab-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="967ab-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="967ab-140">Library</span></span><br/> | <dl> <span data-ttu-id="967ab-141"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="967ab-141"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
