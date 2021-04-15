---
description: 'Метод SetStartStop2 задает время начала и окончания объекта относительно родителя объекта. Этот метод эквивалентен Иамтимелинеобж:: Сетстартстоп, но принимает значения РЕФТИМЕ.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'Метод Иамтимелинеобж:: SetStartStop2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689142"
---
# <a name="iamtimelineobjsetstartstop2-method"></a><span data-ttu-id="5eb47-104">Метод Иамтимелинеобж:: SetStartStop2</span><span class="sxs-lookup"><span data-stu-id="5eb47-104">IAMTimelineObj::SetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="5eb47-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5eb47-105">\[Deprecated.</span></span> <span data-ttu-id="5eb47-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5eb47-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5eb47-107">`SetStartStop2`Метод задает время начала и окончания объекта относительно родителя объекта.</span><span class="sxs-lookup"><span data-stu-id="5eb47-107">The `SetStartStop2` method sets the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="5eb47-108">Этот метод эквивалентен [**иамтимелинеобж:: сетстартстоп**](iamtimelineobj-setstartstop.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="5eb47-108">This method is equivalent to [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb47-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5eb47-109">Syntax</span></span>


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="5eb47-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5eb47-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb47-111">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="5eb47-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="5eb47-112">Новое время запуска в секундах или – 1 для сохранения существующего времени начала.</span><span class="sxs-lookup"><span data-stu-id="5eb47-112">New start time, in seconds, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="5eb47-113">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="5eb47-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="5eb47-114">Новое время окончания, в секундах или – 1 для сохранения текущего времени окончания.</span><span class="sxs-lookup"><span data-stu-id="5eb47-114">New stop time, in seconds, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb47-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5eb47-115">Return value</span></span>

<span data-ttu-id="5eb47-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="5eb47-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="5eb47-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5eb47-117">Return code</span></span>                                                                                  | <span data-ttu-id="5eb47-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5eb47-118">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="5eb47-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5eb47-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5eb47-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5eb47-120">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="5eb47-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5eb47-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5eb47-122">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="5eb47-122">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="5eb47-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="5eb47-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="5eb47-124">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="5eb47-124">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="5eb47-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5eb47-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5eb47-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5eb47-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5eb47-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5eb47-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5eb47-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5eb47-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5eb47-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5eb47-129">Requirements</span></span>



| <span data-ttu-id="5eb47-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5eb47-130">Requirement</span></span> | <span data-ttu-id="5eb47-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5eb47-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb47-132">Header</span><span class="sxs-lookup"><span data-stu-id="5eb47-132">Header</span></span><br/>  | <dl> <span data-ttu-id="5eb47-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb47-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5eb47-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5eb47-134">Library</span></span><br/> | <dl> <span data-ttu-id="5eb47-135"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5eb47-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eb47-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5eb47-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb47-137">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="5eb47-137">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5eb47-138">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5eb47-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




