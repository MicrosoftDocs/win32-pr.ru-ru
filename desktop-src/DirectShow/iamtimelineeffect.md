---
description: Интерфейс Иамтимелиниффект предоставляет методы для управления звуковыми и видеоэффектами в службах редактирования DirectShow (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Интерфейс Иамтимелиниффект (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680072"
---
# <a name="iamtimelineeffect-interface"></a><span data-ttu-id="aed89-103">Интерфейс Иамтимелиниффект</span><span class="sxs-lookup"><span data-stu-id="aed89-103">IAMTimelineEffect interface</span></span>

> [!Note]  
> <span data-ttu-id="aed89-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="aed89-104">\[Deprecated.</span></span> <span data-ttu-id="aed89-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aed89-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aed89-106">`IAMTimelineEffect`Интерфейс предоставляет методы для управления звуковыми и видеоэффектами в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="aed89-106">The `IAMTimelineEffect` interface provides methods for manipulating audio and video effects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="aed89-107">К любому объекту временной шкалы, предоставляющему интерфейс [**иамтимелиниффектабле**](iamtimelineeffectable.md) , можно добавить эффекты.</span><span class="sxs-lookup"><span data-stu-id="aed89-107">An effect can be added to any timeline object that exposes the [**IAMTimelineEffectable**](iamtimelineeffectable.md) interface.</span></span> <span data-ttu-id="aed89-108">Чтобы задать свойства для влияния, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="aed89-108">To set properties on an effect, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="aed89-109">Объект влияния DES на самом деле является оболочкой для одного из двух других объектов:</span><span class="sxs-lookup"><span data-stu-id="aed89-109">The DES effect object is actually a wrapper for one of two other objects:</span></span>

-   <span data-ttu-id="aed89-110">Для звуковых эффектов — любой фильтр звукового эффекта DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aed89-110">For audio effects, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="aed89-111">Для видеоэффектов и 1-входного объекта преобразования DirectX.</span><span class="sxs-lookup"><span data-stu-id="aed89-111">For video effects, and 1-input DirectX Transform object.</span></span>

<span data-ttu-id="aed89-112">Корпорация Майкрософт больше не поддерживает разработку объектов преобразования DirectX сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="aed89-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span>

<span data-ttu-id="aed89-113">Чтобы указать фильтр или объект преобразования DirectX для воздействия, вызовите метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="aed89-113">To specify the filter or DirectX Transform object for an effect, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="aed89-114">Чтобы создать объект Effect, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) с помощью \_ действия основной тип временной шкалы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="aed89-114">To create an effect object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_EFFECT.</span></span> <span data-ttu-id="aed89-115">Вы можете запросить возвращенный указатель [**иамтимелинеобж**](iamtimelineobj.md) для `IAMTimelineEffect` интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aed89-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineEffect` interface.</span></span>

## <a name="members"></a><span data-ttu-id="aed89-116">Элементы</span><span class="sxs-lookup"><span data-stu-id="aed89-116">Members</span></span>

<span data-ttu-id="aed89-117">Интерфейс **иамтимелиниффект** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aed89-117">The **IAMTimelineEffect** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aed89-118">**Иамтимелиниффект** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aed89-118">**IAMTimelineEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="aed89-119">Методы</span><span class="sxs-lookup"><span data-stu-id="aed89-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aed89-120">Методы</span><span class="sxs-lookup"><span data-stu-id="aed89-120">Methods</span></span>

<span data-ttu-id="aed89-121">Интерфейс **иамтимелиниффект** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="aed89-121">The **IAMTimelineEffect** interface has these methods.</span></span>



| <span data-ttu-id="aed89-122">Метод</span><span class="sxs-lookup"><span data-stu-id="aed89-122">Method</span></span>                                                           | <span data-ttu-id="aed89-123">Описание</span><span class="sxs-lookup"><span data-stu-id="aed89-123">Description</span></span>                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="aed89-124">**еффектжетприорити**</span><span class="sxs-lookup"><span data-stu-id="aed89-124">**EffectGetPriority**</span></span>](iamtimelineeffect-effectgetpriority.md) | <span data-ttu-id="aed89-125">Получает уровень приоритета воздействия.</span><span class="sxs-lookup"><span data-stu-id="aed89-125">Retrieves the effect's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aed89-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aed89-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aed89-127">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="aed89-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aed89-128">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aed89-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aed89-129">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="aed89-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aed89-130">Требования</span><span class="sxs-lookup"><span data-stu-id="aed89-130">Requirements</span></span>



| <span data-ttu-id="aed89-131">Требование</span><span class="sxs-lookup"><span data-stu-id="aed89-131">Requirement</span></span> | <span data-ttu-id="aed89-132">Значение</span><span class="sxs-lookup"><span data-stu-id="aed89-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aed89-133">Header</span><span class="sxs-lookup"><span data-stu-id="aed89-133">Header</span></span><br/>  | <dl> <span data-ttu-id="aed89-134"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="aed89-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aed89-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aed89-135">Library</span></span><br/> | <dl> <span data-ttu-id="aed89-136"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aed89-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed89-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aed89-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed89-138">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="aed89-138">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
