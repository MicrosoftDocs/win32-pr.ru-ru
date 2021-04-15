---
description: Метод Рефрешдисплайтипе обновляет видеоформат объекта в соответствии с указанным отображением.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Цимажедисплай. Рефрешдисплайтипе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675773"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a><span data-ttu-id="bffd3-103">Цимажедисплай. Рефрешдисплайтипе, метод</span><span class="sxs-lookup"><span data-stu-id="bffd3-103">CImageDisplay.RefreshDisplayType method</span></span>

<span data-ttu-id="bffd3-104">`RefreshDisplayType`Метод обновляет видеоформат объекта в соответствии с указанным отображением.</span><span class="sxs-lookup"><span data-stu-id="bffd3-104">The `RefreshDisplayType` method updates the object's video format to match the specified display.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffd3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bffd3-105">Syntax</span></span>


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a><span data-ttu-id="bffd3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bffd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bffd3-107">*сздевиценаме*</span><span class="sxs-lookup"><span data-stu-id="bffd3-107">*szDeviceName*</span></span> 
</dt> <dd>

<span data-ttu-id="bffd3-108">Указатель на строку, содержащую имя устройства вывода, которое возвращается функцией GDI **енумдисплайдевицес** .</span><span class="sxs-lookup"><span data-stu-id="bffd3-108">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="bffd3-109">Чтобы использовать основное устройство вывода, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bffd3-109">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bffd3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bffd3-110">Return value</span></span>

<span data-ttu-id="bffd3-111">Возвращает значение \_ ОК, если успешно, или E \_ Fail, если не удалось.</span><span class="sxs-lookup"><span data-stu-id="bffd3-111">Returns S\_OK if successful, or E\_FAIL if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bffd3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bffd3-112">Remarks</span></span>

<span data-ttu-id="bffd3-113">Этот метод инициализирует **\_ отображаемый элемент m** на тип видео, соответствующий режиму экрана на указанном устройстве.</span><span class="sxs-lookup"><span data-stu-id="bffd3-113">This method initializes the **m\_Display** member to a video type that corresponds to the display mode on the specified device.</span></span>

<span data-ttu-id="bffd3-114">Этот метод следует вызывать каждый раз при \_ получении сообщения ДИСПЛАЙЧАНЖЕД WM или при указании дополнительного устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="bffd3-114">Call this method whenever a WM\_DISPLAYCHANGED message is received, or to specify a secondary display device.</span></span>

## <a name="requirements"></a><span data-ttu-id="bffd3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bffd3-115">Requirements</span></span>



| <span data-ttu-id="bffd3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bffd3-116">Requirement</span></span> | <span data-ttu-id="bffd3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bffd3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bffd3-118">Header</span><span class="sxs-lookup"><span data-stu-id="bffd3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bffd3-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bffd3-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bffd3-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bffd3-120">Library</span></span><br/> | <dl> <span data-ttu-id="bffd3-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bffd3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bffd3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bffd3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffd3-123">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="bffd3-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




