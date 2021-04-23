---
description: 'Метод GetSrcAtTime2 извлекает исходный объект, ближайший к заданному времени, в соответствии с указанными условиями границ. Этот метод эквивалентен Иамтимелинетракк:: Жетсркаттиме, но принимает значение РЕФТИМЕ.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'Метод Иамтимелинетракк:: GetSrcAtTime2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675065"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a><span data-ttu-id="041dd-104">Метод Иамтимелинетракк:: GetSrcAtTime2</span><span class="sxs-lookup"><span data-stu-id="041dd-104">IAMTimelineTrack::GetSrcAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="041dd-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="041dd-105">\[Deprecated.</span></span> <span data-ttu-id="041dd-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="041dd-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="041dd-107">`GetSrcAtTime2`Метод получает исходный объект, ближайший к заданному времени, в соответствии с указанными условиями границ.</span><span class="sxs-lookup"><span data-stu-id="041dd-107">The `GetSrcAtTime2` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="041dd-108">Этот метод эквивалентен [**иамтимелинетракк:: жетсркаттиме**](iamtimelinetrack-getsrcattime.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="041dd-108">This method is equivalent to [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="041dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="041dd-109">Syntax</span></span>


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="041dd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="041dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="041dd-111">*ппсрк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="041dd-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="041dd-112">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="041dd-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="041dd-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="041dd-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="041dd-114">Время начала поиска в секундах.</span><span class="sxs-lookup"><span data-stu-id="041dd-114">Start time for the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="041dd-115">*сеарчдиректион*</span><span class="sxs-lookup"><span data-stu-id="041dd-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="041dd-116">Член перечисляемого типа [**декстерф \_ Track \_ Search \_ flags**](dexterf-track-search-flags.md) , указывающий условия границ для поиска.</span><span class="sxs-lookup"><span data-stu-id="041dd-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="041dd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="041dd-117">Return value</span></span>

<span data-ttu-id="041dd-118">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="041dd-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="041dd-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="041dd-119">Return code</span></span>                                                                                  | <span data-ttu-id="041dd-120">Описание</span><span class="sxs-lookup"><span data-stu-id="041dd-120">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="041dd-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="041dd-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="041dd-122">Не удалось располагать исходный объект.</span><span class="sxs-lookup"><span data-stu-id="041dd-122">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="041dd-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="041dd-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="041dd-124">Расположение исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="041dd-124">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="041dd-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="041dd-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="041dd-126">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="041dd-126">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="041dd-127"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="041dd-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="041dd-128">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="041dd-128">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="041dd-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="041dd-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="041dd-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="041dd-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="041dd-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="041dd-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="041dd-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="041dd-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="041dd-133">Требования</span><span class="sxs-lookup"><span data-stu-id="041dd-133">Requirements</span></span>



| <span data-ttu-id="041dd-134">Требование</span><span class="sxs-lookup"><span data-stu-id="041dd-134">Requirement</span></span> | <span data-ttu-id="041dd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="041dd-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="041dd-136">Header</span><span class="sxs-lookup"><span data-stu-id="041dd-136">Header</span></span><br/>  | <dl> <span data-ttu-id="041dd-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="041dd-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="041dd-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="041dd-138">Library</span></span><br/> | <dl> <span data-ttu-id="041dd-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="041dd-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="041dd-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="041dd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041dd-141">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="041dd-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="041dd-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="041dd-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




