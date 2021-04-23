---
description: Метод Фикстимес Округляет указанное время начала и окончания до ближайших границ фрейма, как определено параметром частоты кадров родительской группы.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'Метод Иамтимелинеобж:: Фикстимес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689483"
---
# <a name="iamtimelineobjfixtimes-method"></a><span data-ttu-id="c2457-103">Метод Иамтимелинеобж:: Фикстимес</span><span class="sxs-lookup"><span data-stu-id="c2457-103">IAMTimelineObj::FixTimes method</span></span>

> [!Note]  
> <span data-ttu-id="c2457-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c2457-104">\[Deprecated.</span></span> <span data-ttu-id="c2457-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2457-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c2457-106">`FixTimes`Метод Округляет указанное время начала и окончания до ближайших границ фрейма, как определено параметром частоты кадров родительской группы.</span><span class="sxs-lookup"><span data-stu-id="c2457-106">The `FixTimes` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2457-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2457-107">Syntax</span></span>


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="c2457-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2457-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2457-109">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="c2457-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c2457-110">Указатель на переменную, которая содержит время начала (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="c2457-110">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="c2457-111">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="c2457-111">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="c2457-112">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="c2457-112">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c2457-113">Указатель на переменную, которая содержит время окончания в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="c2457-113">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="c2457-114">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="c2457-114">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2457-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2457-115">Return value</span></span>

<span data-ttu-id="c2457-116">Возвращает \_ ОК в случае успеха или E \_ нотинтри, если объект не является частью группы.</span><span class="sxs-lookup"><span data-stu-id="c2457-116">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2457-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2457-117">Remarks</span></span>

<span data-ttu-id="c2457-118">Во время подготовки к просмотру DES округляет время начала и окончания объекта до ближайшей границы фрейма.</span><span class="sxs-lookup"><span data-stu-id="c2457-118">During rendering, DES rounds the object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="c2457-119">Однако DES не перезаписывает время объекта.</span><span class="sxs-lookup"><span data-stu-id="c2457-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="c2457-120">При изменении частоты кадров группы округленные значения всегда вычисляются исходя из исходного времени.</span><span class="sxs-lookup"><span data-stu-id="c2457-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="c2457-121">Дополнительные сведения см. [в разделе время в службах редактирования DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="c2457-121">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="c2457-122">Используйте этот метод, чтобы определить точное время начала и окончания работы в проекте, готовом для просмотра.</span><span class="sxs-lookup"><span data-stu-id="c2457-122">Use this method to determine accurate start and stop times in the rendered project.</span></span> <span data-ttu-id="c2457-123">Например, следует перейти к округленному времени, а не к исходному времени начала и окончания объекта.</span><span class="sxs-lookup"><span data-stu-id="c2457-123">For example, you should seek to the rounded times, rather than the object's original start and stop times.</span></span> <span data-ttu-id="c2457-124">Вызовите [**иамтимелинеобж:: жетстартстоп**](iamtimelineobj-getstartstop.md) , чтобы получить исходное значение времени, и передайте эти значения в `FixTimes` .</span><span class="sxs-lookup"><span data-stu-id="c2457-124">Call [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) to obtain the original times, and pass those values to `FixTimes`.</span></span>

> [!Note]  
> <span data-ttu-id="c2457-125">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c2457-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c2457-126">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2457-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c2457-127">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c2457-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2457-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c2457-128">Requirements</span></span>



| <span data-ttu-id="c2457-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c2457-129">Requirement</span></span> | <span data-ttu-id="c2457-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c2457-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2457-131">Header</span><span class="sxs-lookup"><span data-stu-id="c2457-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c2457-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2457-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c2457-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2457-133">Library</span></span><br/> | <dl> <span data-ttu-id="c2457-134"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2457-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2457-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2457-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2457-136">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="c2457-136">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c2457-137">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="c2457-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




