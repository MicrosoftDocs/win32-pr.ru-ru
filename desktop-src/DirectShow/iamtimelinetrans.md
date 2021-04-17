---
description: Интерфейс Иамтимелинетранс предоставляет методы для управления переходами в службах редактирования DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Интерфейс Иамтимелинетранс (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689420"
---
# <a name="iamtimelinetrans-interface"></a><span data-ttu-id="bf5cf-103">Интерфейс Иамтимелинетранс</span><span class="sxs-lookup"><span data-stu-id="bf5cf-103">IAMTimelineTrans interface</span></span>

> [!Note]  
> <span data-ttu-id="bf5cf-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-104">\[Deprecated.</span></span> <span data-ttu-id="bf5cf-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bf5cf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bf5cf-106">`IAMTimelineTrans`Интерфейс предоставляет методы для управления переходами в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="bf5cf-106">The `IAMTimelineTrans` interface provides methods for manipulating transitions in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="bf5cf-107">Переход — это ход выполнения между одним видеослоем и визуализированным совмещением всех слоев видео с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-107">A transition is a progression between one video layer and the rendered composite of all video layers with a lower priority.</span></span> <span data-ttu-id="bf5cf-108">Переход можно добавить к любому объекту временной шкалы, предоставляющему интерфейс [**иамтимелинетрансабле**](iamtimelinetransable.md) .</span><span class="sxs-lookup"><span data-stu-id="bf5cf-108">A transition can be added to any timeline object that exposes the [**IAMTimelineTransable**](iamtimelinetransable.md) interface.</span></span> <span data-ttu-id="bf5cf-109">Чтобы задать свойства перехода, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="bf5cf-109">To set properties on a transition, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="bf5cf-110">Объект перехода DES на самом деле является оболочкой для объекта преобразования DirectX.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-110">The DES transition object is actually a wrapper for a DirectX Transform object.</span></span> <span data-ttu-id="bf5cf-111">Любой из двух входных объектов DirectX Transform можно использовать для реализации визуального влияния перехода.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-111">Any 2-input DirectX Transform object can be used to implement the visual effect for the transition.</span></span> <span data-ttu-id="bf5cf-112">Корпорация Майкрософт больше не поддерживает разработку объектов преобразования DirectX сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="bf5cf-113">Чтобы указать объект преобразования DirectX для перехода, вызовите метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="bf5cf-113">To specify the DirectX Transform object for a transition, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="bf5cf-114">Чтобы создать объект перехода, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) с переходом на значение основного типа временной шкалы \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bf5cf-114">To create a transition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRANSITION.</span></span> <span data-ttu-id="bf5cf-115">Вы можете запросить возвращенный указатель [**иамтимелинеобж**](iamtimelineobj.md) для `IAMTimelineTrans` интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineTrans` interface.</span></span>

## <a name="members"></a><span data-ttu-id="bf5cf-116">Элементы</span><span class="sxs-lookup"><span data-stu-id="bf5cf-116">Members</span></span>

<span data-ttu-id="bf5cf-117">Интерфейс **иамтимелинетранс** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bf5cf-117">The **IAMTimelineTrans** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bf5cf-118">**Иамтимелинетранс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bf5cf-118">**IAMTimelineTrans** also has these types of members:</span></span>

-   [<span data-ttu-id="bf5cf-119">Методы</span><span class="sxs-lookup"><span data-stu-id="bf5cf-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bf5cf-120">Методы</span><span class="sxs-lookup"><span data-stu-id="bf5cf-120">Methods</span></span>

<span data-ttu-id="bf5cf-121">Интерфейс **иамтимелинетранс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-121">The **IAMTimelineTrans** interface has these methods.</span></span>



| <span data-ttu-id="bf5cf-122">Метод</span><span class="sxs-lookup"><span data-stu-id="bf5cf-122">Method</span></span>                                                  | <span data-ttu-id="bf5cf-123">Описание</span><span class="sxs-lookup"><span data-stu-id="bf5cf-123">Description</span></span>                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf5cf-124">**жеткутпоинт**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-124">**GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)     | <span data-ttu-id="bf5cf-125">Извлекает вырезанную точку.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-125">Retrieves the cut point.</span></span><br/>                                                    |
| [<span data-ttu-id="bf5cf-126">**GetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-126">**GetCutPoint2**</span></span>](iamtimelinetrans-getcutpoint2.md)   | <span data-ttu-id="bf5cf-127">Извлекает вырезанную точку в виде значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="bf5cf-127">Retrieves the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>             |
| [<span data-ttu-id="bf5cf-128">**жеткутсонли**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-128">**GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)     | <span data-ttu-id="bf5cf-129">Определяет, визуализируется ли переход как вырезание.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-129">Determines whether the transition is rendered as a cut.</span></span><br/>                     |
| [<span data-ttu-id="bf5cf-130">**жетсвапинпутс**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-130">**GetSwapInputs**</span></span>](iamtimelinetrans-getswapinputs.md) | <span data-ttu-id="bf5cf-131">Извлекает значение, указывающее, меняются ли входные данные перехода.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-131">Retrieves a value that indicates whether the transition inputs are swapped.</span></span><br/> |
| [<span data-ttu-id="bf5cf-132">**сеткутпоинт**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-132">**SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)     | <span data-ttu-id="bf5cf-133">Задает точку вырезания.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-133">Sets the cut point.</span></span><br/>                                                         |
| [<span data-ttu-id="bf5cf-134">**SetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-134">**SetCutPoint2**</span></span>](iamtimelinetrans-setcutpoint2.md)   | <span data-ttu-id="bf5cf-135">Задает точку вырезания как значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="bf5cf-135">Sets the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>                  |
| [<span data-ttu-id="bf5cf-136">**сеткутсонли**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-136">**SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)     | <span data-ttu-id="bf5cf-137">Указывает, визуализируется ли переход как вырезание.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-137">Specifies whether the transition is rendered as a cut.</span></span><br/>                      |
| [<span data-ttu-id="bf5cf-138">**сетсвапинпутс**</span><span class="sxs-lookup"><span data-stu-id="bf5cf-138">**SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md) | <span data-ttu-id="bf5cf-139">Указывает, меняются ли входные данные перехода.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-139">Specifies whether the transition inputs are swapped.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="bf5cf-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf5cf-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf5cf-141">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="bf5cf-141">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bf5cf-142">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bf5cf-142">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bf5cf-143">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="bf5cf-143">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf5cf-144">Требования</span><span class="sxs-lookup"><span data-stu-id="bf5cf-144">Requirements</span></span>



| <span data-ttu-id="bf5cf-145">Требование</span><span class="sxs-lookup"><span data-stu-id="bf5cf-145">Requirement</span></span> | <span data-ttu-id="bf5cf-146">Значение</span><span class="sxs-lookup"><span data-stu-id="bf5cf-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5cf-147">Header</span><span class="sxs-lookup"><span data-stu-id="bf5cf-147">Header</span></span><br/>  | <dl> <span data-ttu-id="bf5cf-148"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf5cf-148"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bf5cf-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf5cf-149">Library</span></span><br/> | <dl> <span data-ttu-id="bf5cf-150"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf5cf-150"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf5cf-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf5cf-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf5cf-152">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="bf5cf-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
