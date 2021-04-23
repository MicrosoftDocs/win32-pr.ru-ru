---
description: 'Метод GetTransAtTime2 извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ. Этот метод эквивалентен Иамтимелинетрансабле:: Жеттрансаттиме, но принимает параметр РЕФТИМЕ.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Метод Иамтимелинетрансабле:: GetTransAtTime2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689415"
---
# <a name="iamtimelinetransablegettransattime2-method"></a><span data-ttu-id="47f05-104">Метод Иамтимелинетрансабле:: GetTransAtTime2</span><span class="sxs-lookup"><span data-stu-id="47f05-104">IAMTimelineTransable::GetTransAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="47f05-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="47f05-105">\[Deprecated.</span></span> <span data-ttu-id="47f05-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47f05-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="47f05-107">`GetTransAtTime2`Метод извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ.</span><span class="sxs-lookup"><span data-stu-id="47f05-107">The `GetTransAtTime2` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="47f05-108">Этот метод эквивалентен [**иамтимелинетрансабле:: жеттрансаттиме**](iamtimelinetransable-gettransattime.md), но принимает параметр [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="47f05-108">This method is equivalent to [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), but takes a [**REFTIME**](reftime.md) parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f05-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47f05-109">Syntax</span></span>


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="47f05-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="47f05-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f05-111">*ппобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="47f05-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f05-112">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) перехода.</span><span class="sxs-lookup"><span data-stu-id="47f05-112">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="47f05-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="47f05-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="47f05-114">Время начала поиска в секундах.</span><span class="sxs-lookup"><span data-stu-id="47f05-114">Time from which to begin the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="47f05-115">*сеарчдиректион*</span><span class="sxs-lookup"><span data-stu-id="47f05-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="47f05-116">Член перечисляемого типа [**декстерф \_ Track \_ Search \_ flags**](dexterf-track-search-flags.md) , указывающий условия границ для поиска.</span><span class="sxs-lookup"><span data-stu-id="47f05-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f05-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47f05-117">Return value</span></span>

<span data-ttu-id="47f05-118">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="47f05-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="47f05-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="47f05-119">Return code</span></span>                                                                                  | <span data-ttu-id="47f05-120">Описание</span><span class="sxs-lookup"><span data-stu-id="47f05-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="47f05-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="47f05-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="47f05-122">Переход не найден.</span><span class="sxs-lookup"><span data-stu-id="47f05-122">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="47f05-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="47f05-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="47f05-124">Обнаружен переход.</span><span class="sxs-lookup"><span data-stu-id="47f05-124">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="47f05-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47f05-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="47f05-126">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="47f05-126">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="47f05-127"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="47f05-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="47f05-128">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="47f05-128">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47f05-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47f05-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="47f05-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="47f05-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="47f05-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="47f05-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="47f05-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="47f05-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="47f05-133">Требования</span><span class="sxs-lookup"><span data-stu-id="47f05-133">Requirements</span></span>



| <span data-ttu-id="47f05-134">Требование</span><span class="sxs-lookup"><span data-stu-id="47f05-134">Requirement</span></span> | <span data-ttu-id="47f05-135">Значение</span><span class="sxs-lookup"><span data-stu-id="47f05-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47f05-136">Header</span><span class="sxs-lookup"><span data-stu-id="47f05-136">Header</span></span><br/>  | <dl> <span data-ttu-id="47f05-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f05-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="47f05-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47f05-138">Library</span></span><br/> | <dl> <span data-ttu-id="47f05-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47f05-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f05-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47f05-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f05-141">**Интерфейс Иамтимелинетрансабле**</span><span class="sxs-lookup"><span data-stu-id="47f05-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="47f05-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="47f05-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




