---
description: Метод Жеттрансаттиме извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'Метод Иамтимелинетрансабле:: Жеттрансаттиме (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689416"
---
# <a name="iamtimelinetransablegettransattime-method"></a><span data-ttu-id="cd4e9-103">Метод Иамтимелинетрансабле:: Жеттрансаттиме</span><span class="sxs-lookup"><span data-stu-id="cd4e9-103">IAMTimelineTransable::GetTransAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="cd4e9-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-104">\[Deprecated.</span></span> <span data-ttu-id="cd4e9-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cd4e9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cd4e9-106">`GetTransAtTime`Метод извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-106">The `GetTransAtTime` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd4e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd4e9-107">Syntax</span></span>


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="cd4e9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd4e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd4e9-109">*ппобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cd4e9-109">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd4e9-110">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) перехода.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-110">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cd4e9-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="cd4e9-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="cd4e9-112">Время, с которого начинается поиск, в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-112">Time from which to begin the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="cd4e9-113">*сеарчдиректион*</span><span class="sxs-lookup"><span data-stu-id="cd4e9-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="cd4e9-114">Член перечисляемого типа [**декстерф \_ Track \_ Search \_ flags**](dexterf-track-search-flags.md) , указывающий условия границ для поиска.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd4e9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd4e9-115">Return value</span></span>

<span data-ttu-id="cd4e9-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="cd4e9-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="cd4e9-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cd4e9-117">Return code</span></span>                                                                                  | <span data-ttu-id="cd4e9-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cd4e9-118">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="cd4e9-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e9-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="cd4e9-120">Переход не найден.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-120">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="cd4e9-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e9-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cd4e9-122">Обнаружен переход.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-122">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="cd4e9-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e9-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cd4e9-124">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-124">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="cd4e9-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e9-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="cd4e9-126">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd4e9-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd4e9-127">Remarks</span></span>

<span data-ttu-id="cd4e9-128">Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="cd4e9-129">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="cd4e9-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cd4e9-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cd4e9-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cd4e9-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cd4e9-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cd4e9-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cd4e9-133">Требования</span><span class="sxs-lookup"><span data-stu-id="cd4e9-133">Requirements</span></span>



| <span data-ttu-id="cd4e9-134">Требование</span><span class="sxs-lookup"><span data-stu-id="cd4e9-134">Requirement</span></span> | <span data-ttu-id="cd4e9-135">Значение</span><span class="sxs-lookup"><span data-stu-id="cd4e9-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd4e9-136">Header</span><span class="sxs-lookup"><span data-stu-id="cd4e9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="cd4e9-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e9-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cd4e9-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd4e9-138">Library</span></span><br/> | <dl> <span data-ttu-id="cd4e9-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e9-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd4e9-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd4e9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd4e9-141">**Интерфейс Иамтимелинетрансабле**</span><span class="sxs-lookup"><span data-stu-id="cd4e9-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="cd4e9-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="cd4e9-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




