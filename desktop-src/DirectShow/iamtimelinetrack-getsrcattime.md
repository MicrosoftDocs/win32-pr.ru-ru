---
description: Метод Жетсркаттиме извлекает исходный объект, ближайший к заданному времени, в соответствии с указанными условиями границ.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'Метод Иамтимелинетракк:: Жетсркаттиме (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685237"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a><span data-ttu-id="74448-103">Метод Иамтимелинетракк:: Жетсркаттиме</span><span class="sxs-lookup"><span data-stu-id="74448-103">IAMTimelineTrack::GetSrcAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="74448-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="74448-104">\[Deprecated.</span></span> <span data-ttu-id="74448-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74448-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="74448-106">`GetSrcAtTime`Метод получает исходный объект, ближайший к заданному времени, в соответствии с указанными условиями границ.</span><span class="sxs-lookup"><span data-stu-id="74448-106">The `GetSrcAtTime` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="74448-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74448-107">Syntax</span></span>


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="74448-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="74448-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74448-109">*ппсрк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="74448-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74448-110">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="74448-110">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="74448-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="74448-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="74448-112">Время начала поиска в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="74448-112">Start time for the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="74448-113">*сеарчдиректион*</span><span class="sxs-lookup"><span data-stu-id="74448-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="74448-114">Член перечисляемого типа [**декстерф \_ Track \_ Search \_ flags**](dexterf-track-search-flags.md) , указывающий условия границ для поиска.</span><span class="sxs-lookup"><span data-stu-id="74448-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74448-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74448-115">Return value</span></span>

<span data-ttu-id="74448-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="74448-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="74448-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="74448-117">Return code</span></span>                                                                                  | <span data-ttu-id="74448-118">Описание</span><span class="sxs-lookup"><span data-stu-id="74448-118">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="74448-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="74448-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="74448-120">Не удалось располагать исходный объект.</span><span class="sxs-lookup"><span data-stu-id="74448-120">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="74448-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="74448-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="74448-122">Расположение исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="74448-122">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="74448-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="74448-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="74448-124">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="74448-124">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="74448-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="74448-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="74448-126">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="74448-126">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="74448-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74448-127">Remarks</span></span>

<span data-ttu-id="74448-128">Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="74448-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="74448-129">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="74448-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="74448-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="74448-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="74448-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="74448-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="74448-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="74448-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="74448-133">Требования</span><span class="sxs-lookup"><span data-stu-id="74448-133">Requirements</span></span>



| <span data-ttu-id="74448-134">Требование</span><span class="sxs-lookup"><span data-stu-id="74448-134">Requirement</span></span> | <span data-ttu-id="74448-135">Значение</span><span class="sxs-lookup"><span data-stu-id="74448-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74448-136">Header</span><span class="sxs-lookup"><span data-stu-id="74448-136">Header</span></span><br/>  | <dl> <span data-ttu-id="74448-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="74448-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="74448-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74448-138">Library</span></span><br/> | <dl> <span data-ttu-id="74448-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74448-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74448-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74448-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74448-141">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="74448-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="74448-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="74448-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




