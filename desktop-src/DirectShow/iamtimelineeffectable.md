---
description: Интерфейс Иамтимелиниффектабле предоставляет методы для добавления эффектов к объекту временной шкалы в службах редактирования DirectShow (DES) и для управления эффектами на объекте.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Интерфейс Иамтимелиниффектабле (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675507"
---
# <a name="iamtimelineeffectable-interface"></a><span data-ttu-id="f54aa-103">Интерфейс Иамтимелиниффектабле</span><span class="sxs-lookup"><span data-stu-id="f54aa-103">IAMTimelineEffectable interface</span></span>

> [!Note]  
> <span data-ttu-id="f54aa-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f54aa-104">\[Deprecated.</span></span> <span data-ttu-id="f54aa-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f54aa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f54aa-106">`IAMTimelineEffectable`Интерфейс предоставляет методы для добавления эффектов к объекту временной шкалы в [службах редактирования DirectShow](directshow-editing-services.md) (DES), а также для управления эффектами на объекте.</span><span class="sxs-lookup"><span data-stu-id="f54aa-106">The `IAMTimelineEffectable` interface provides methods for adding effects to a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES), and for manipulating the effects on an object.</span></span> <span data-ttu-id="f54aa-107">Этот интерфейс реализуется всеми объектами, к которым могут применяться эффекты. Сюда входят источники, дорожки и композиции.</span><span class="sxs-lookup"><span data-stu-id="f54aa-107">All objects that can have effects applied to them implement this interface; this includes sources, tracks, and compositions.</span></span>

<span data-ttu-id="f54aa-108">Объект, реализующий этот интерфейс, может иметь любое количество эффектов.</span><span class="sxs-lookup"><span data-stu-id="f54aa-108">An object that implements this interface can have any number of effects.</span></span> <span data-ttu-id="f54aa-109">Для каждого объекта механизм визуализации применяет свои эффекты в порядке приоритета, начиная с уровня приоритета 0.</span><span class="sxs-lookup"><span data-stu-id="f54aa-109">For each object, the render engine applies its effects in order of priority, starting with priority level 0.</span></span>

## <a name="members"></a><span data-ttu-id="f54aa-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="f54aa-110">Members</span></span>

<span data-ttu-id="f54aa-111">Интерфейс **иамтимелиниффектабле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f54aa-111">The **IAMTimelineEffectable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f54aa-112">**Иамтимелиниффектабле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f54aa-112">**IAMTimelineEffectable** also has these types of members:</span></span>

-   [<span data-ttu-id="f54aa-113">Методы</span><span class="sxs-lookup"><span data-stu-id="f54aa-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f54aa-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f54aa-114">Methods</span></span>

<span data-ttu-id="f54aa-115">Интерфейс **иамтимелиниффектабле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f54aa-115">The **IAMTimelineEffectable** interface has these methods.</span></span>



| <span data-ttu-id="f54aa-116">Метод</span><span class="sxs-lookup"><span data-stu-id="f54aa-116">Method</span></span>                                                                     | <span data-ttu-id="f54aa-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f54aa-117">Description</span></span>                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="f54aa-118">**еффектжеткаунт**</span><span class="sxs-lookup"><span data-stu-id="f54aa-118">**EffectGetCount**</span></span>](iamtimelineeffectable-effectgetcount.md)             | <span data-ttu-id="f54aa-119">Возвращает количество эффектов для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="f54aa-119">Retrieves the number of effects on this object.</span></span><br/>                    |
| [<span data-ttu-id="f54aa-120">**еффектинсбефоре**</span><span class="sxs-lookup"><span data-stu-id="f54aa-120">**EffectInsBefore**</span></span>](iamtimelineeffectable-effectinsbefore.md)           | <span data-ttu-id="f54aa-121">Вставляет результат в объект с указанным уровнем приоритета.</span><span class="sxs-lookup"><span data-stu-id="f54aa-121">Inserts an effect into the object at the specified priority level.</span></span><br/> |
| [<span data-ttu-id="f54aa-122">**еффектсвапприоритиес**</span><span class="sxs-lookup"><span data-stu-id="f54aa-122">**EffectSwapPriorities**</span></span>](iamtimelineeffectable-effectswappriorities.md) | <span data-ttu-id="f54aa-123">Переключает уровни приоритета двух эффектов.</span><span class="sxs-lookup"><span data-stu-id="f54aa-123">Switches the priority levels of two effects.</span></span><br/>                       |
| [<span data-ttu-id="f54aa-124">**Действие**</span><span class="sxs-lookup"><span data-stu-id="f54aa-124">**GetEffect**</span></span>](iamtimelineeffectable-geteffect.md)                       | <span data-ttu-id="f54aa-125">Получает результат на указанном уровне приоритета.</span><span class="sxs-lookup"><span data-stu-id="f54aa-125">Retrieves the effect at the specified priority level.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="f54aa-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f54aa-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f54aa-127">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f54aa-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f54aa-128">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f54aa-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f54aa-129">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f54aa-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f54aa-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f54aa-130">Requirements</span></span>



| <span data-ttu-id="f54aa-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f54aa-131">Requirement</span></span> | <span data-ttu-id="f54aa-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f54aa-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f54aa-133">Header</span><span class="sxs-lookup"><span data-stu-id="f54aa-133">Header</span></span><br/>  | <dl> <span data-ttu-id="f54aa-134"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f54aa-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f54aa-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f54aa-135">Library</span></span><br/> | <dl> <span data-ttu-id="f54aa-136"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f54aa-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
