---
description: Метод Модифистоптиме задает время окончания относительно временной шкалы.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'Метод Иамтимелинесрк:: Модифистоптиме (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679888"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a><span data-ttu-id="244af-103">Метод Иамтимелинесрк:: Модифистоптиме</span><span class="sxs-lookup"><span data-stu-id="244af-103">IAMTimelineSrc::ModifyStopTime method</span></span>

> [!Note]  
> <span data-ttu-id="244af-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="244af-104">\[Deprecated.</span></span> <span data-ttu-id="244af-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="244af-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="244af-106">`ModifyStopTime`Метод задает время окончания относительно временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="244af-106">The `ModifyStopTime` method sets the stop time, relative to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="244af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="244af-107">Syntax</span></span>


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="244af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="244af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244af-109">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="244af-109">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="244af-110">Новое время окончания в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="244af-110">New stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244af-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="244af-111">Return value</span></span>

<span data-ttu-id="244af-112">Возвращает значение S \_ ОК или E \_ INVALIDARG, если указанное время недопустимо.</span><span class="sxs-lookup"><span data-stu-id="244af-112">Returns S\_OK, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="244af-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="244af-113">Remarks</span></span>

<span data-ttu-id="244af-114">Этот метод эквивалентен вызову [**иамтимелинеобж:: сетстартстоп**](iamtimelineobj-setstartstop.md) с исходным временем начала и новым временем окончания.</span><span class="sxs-lookup"><span data-stu-id="244af-114">This method is equivalent to calling [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) with the original start time and a new stop time.</span></span>

> [!Note]  
> <span data-ttu-id="244af-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="244af-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="244af-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="244af-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="244af-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="244af-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="244af-118">Требования</span><span class="sxs-lookup"><span data-stu-id="244af-118">Requirements</span></span>



| <span data-ttu-id="244af-119">Требование</span><span class="sxs-lookup"><span data-stu-id="244af-119">Requirement</span></span> | <span data-ttu-id="244af-120">Значение</span><span class="sxs-lookup"><span data-stu-id="244af-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="244af-121">Header</span><span class="sxs-lookup"><span data-stu-id="244af-121">Header</span></span><br/>  | <dl> <span data-ttu-id="244af-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="244af-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="244af-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="244af-123">Library</span></span><br/> | <dl> <span data-ttu-id="244af-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="244af-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="244af-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="244af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244af-126">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="244af-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="244af-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="244af-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




