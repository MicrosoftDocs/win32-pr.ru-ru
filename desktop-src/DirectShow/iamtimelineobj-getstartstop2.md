---
description: 'Метод GetStartStop2 извлекает значения времени начала и окончания объекта относительно родителя объекта. Этот метод эквивалентен Иамтимелинеобж:: Жетстартстоп, но принимает значения РЕФТИМЕ.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'Метод Иамтимелинеобж:: GetStartStop2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685395"
---
# <a name="iamtimelineobjgetstartstop2-method"></a><span data-ttu-id="c7714-104">Метод Иамтимелинеобж:: GetStartStop2</span><span class="sxs-lookup"><span data-stu-id="c7714-104">IAMTimelineObj::GetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="c7714-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c7714-105">\[Deprecated.</span></span> <span data-ttu-id="c7714-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7714-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c7714-107">`GetStartStop2`Метод получает значения времени начала и окончания объекта относительно родителя объекта.</span><span class="sxs-lookup"><span data-stu-id="c7714-107">The `GetStartStop2` method retrieves the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="c7714-108">Этот метод эквивалентен [**иамтимелинеобж:: жетстартстоп**](iamtimelineobj-getstartstop.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="c7714-108">This method is equivalent to [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7714-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7714-109">Syntax</span></span>


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="c7714-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7714-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7714-111">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="c7714-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c7714-112">Получает время начала в секундах.</span><span class="sxs-lookup"><span data-stu-id="c7714-112">Receives the start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c7714-113">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="c7714-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c7714-114">Получает время окончания в секундах.</span><span class="sxs-lookup"><span data-stu-id="c7714-114">Receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7714-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7714-115">Return value</span></span>

<span data-ttu-id="c7714-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c7714-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7714-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7714-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7714-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7714-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c7714-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c7714-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7714-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c7714-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c7714-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c7714-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7714-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c7714-122">Requirements</span></span>



| <span data-ttu-id="c7714-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c7714-123">Requirement</span></span> | <span data-ttu-id="c7714-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c7714-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7714-125">Header</span><span class="sxs-lookup"><span data-stu-id="c7714-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c7714-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7714-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c7714-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7714-127">Library</span></span><br/> | <dl> <span data-ttu-id="c7714-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7714-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7714-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7714-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7714-130">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="c7714-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c7714-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="c7714-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




