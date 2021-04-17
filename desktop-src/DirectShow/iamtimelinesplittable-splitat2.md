---
description: 'Метод SplitAt2 разделяет объект в указанное время. Этот метод эквивалентен Иамтимелинесплиттабле:: Сплитат, но принимает значение РЕФТИМЕ.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'Метод Иамтимелинесплиттабле:: SplitAt2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675081"
---
# <a name="iamtimelinesplittablesplitat2-method"></a><span data-ttu-id="c780a-104">Метод Иамтимелинесплиттабле:: SplitAt2</span><span class="sxs-lookup"><span data-stu-id="c780a-104">IAMTimelineSplittable::SplitAt2 method</span></span>

> [!Note]  
> <span data-ttu-id="c780a-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c780a-105">\[Deprecated.</span></span> <span data-ttu-id="c780a-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c780a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c780a-107">`SplitAt2`Метод разделяет объект в указанное время.</span><span class="sxs-lookup"><span data-stu-id="c780a-107">The `SplitAt2` method splits the object at the specified time.</span></span> <span data-ttu-id="c780a-108">Этот метод эквивалентен [**иамтимелинесплиттабле:: сплитат**](iamtimelinesplittable-splitat.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="c780a-108">This method is equivalent to [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c780a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c780a-109">Syntax</span></span>


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="c780a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c780a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c780a-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="c780a-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="c780a-112">Время разделения объекта относительно начала временной шкалы в секундах.</span><span class="sxs-lookup"><span data-stu-id="c780a-112">Time at which to split the object, relative to the start of the timeline, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c780a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c780a-113">Return value</span></span>

<span data-ttu-id="c780a-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c780a-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c780a-115">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="c780a-115">Possible values include the following:</span></span>



| <span data-ttu-id="c780a-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c780a-116">Return code</span></span>                                                                                   | <span data-ttu-id="c780a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c780a-117">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c780a-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c780a-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="c780a-119">Нет для разбиения.</span><span class="sxs-lookup"><span data-stu-id="c780a-119">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="c780a-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c780a-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c780a-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c780a-121">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="c780a-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c780a-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c780a-123">В данный момент объект не существует.</span><span class="sxs-lookup"><span data-stu-id="c780a-123">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="c780a-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c780a-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c780a-125">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="c780a-125">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c780a-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c780a-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c780a-127">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c780a-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c780a-128">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c780a-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c780a-129">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c780a-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c780a-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c780a-130">Requirements</span></span>



| <span data-ttu-id="c780a-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c780a-131">Requirement</span></span> | <span data-ttu-id="c780a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c780a-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c780a-133">Header</span><span class="sxs-lookup"><span data-stu-id="c780a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c780a-134"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c780a-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c780a-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c780a-135">Library</span></span><br/> | <dl> <span data-ttu-id="c780a-136"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c780a-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c780a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c780a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c780a-138">**Интерфейс Иамтимелинесплиттабле**</span><span class="sxs-lookup"><span data-stu-id="c780a-138">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="c780a-139">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="c780a-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




