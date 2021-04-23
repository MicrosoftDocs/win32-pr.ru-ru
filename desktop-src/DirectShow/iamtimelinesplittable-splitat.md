---
description: Метод Сплитат разделяет объект в указанное время.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'Метод Иамтимелинесплиттабле:: Сплитат (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688968"
---
# <a name="iamtimelinesplittablesplitat-method"></a><span data-ttu-id="f60b4-103">Метод Иамтимелинесплиттабле:: Сплитат</span><span class="sxs-lookup"><span data-stu-id="f60b4-103">IAMTimelineSplittable::SplitAt method</span></span>

> [!Note]  
> <span data-ttu-id="f60b4-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f60b4-104">\[Deprecated.</span></span> <span data-ttu-id="f60b4-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f60b4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f60b4-106">`SplitAt`Метод разделяет объект в указанное время.</span><span class="sxs-lookup"><span data-stu-id="f60b4-106">The `SplitAt` method splits the object at the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f60b4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f60b4-107">Syntax</span></span>


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="f60b4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f60b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f60b4-109">*Time*</span><span class="sxs-lookup"><span data-stu-id="f60b4-109">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="f60b4-110">Время разделения объекта относительно начала временной шкалы в единицах с частотой 100 нс.</span><span class="sxs-lookup"><span data-stu-id="f60b4-110">Time at which to split the object, relative to the start of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f60b4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f60b4-111">Return value</span></span>

<span data-ttu-id="f60b4-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f60b4-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f60b4-113">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="f60b4-113">Possible values include the following:</span></span>



| <span data-ttu-id="f60b4-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f60b4-114">Return code</span></span>                                                                                   | <span data-ttu-id="f60b4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f60b4-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="f60b4-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f60b4-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="f60b4-117">Нет для разбиения.</span><span class="sxs-lookup"><span data-stu-id="f60b4-117">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="f60b4-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f60b4-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f60b4-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f60b4-119">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="f60b4-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f60b4-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f60b4-121">В данный момент объект не существует.</span><span class="sxs-lookup"><span data-stu-id="f60b4-121">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="f60b4-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f60b4-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f60b4-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="f60b4-123">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f60b4-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f60b4-124">Remarks</span></span>

<span data-ttu-id="f60b4-125">При разделении источника, воздействия или перехода этот метод создает второй объект того же типа.</span><span class="sxs-lookup"><span data-stu-id="f60b4-125">If you split a source, effect, or transition, this method creates a second object of the same type.</span></span> <span data-ttu-id="f60b4-126">Исходный объект усекается в указанное время разбиения, а новый объект заменяет обрезанную часть.</span><span class="sxs-lookup"><span data-stu-id="f60b4-126">The original object is truncated at the specified split time, and the new object replaces the truncated portion.</span></span> <span data-ttu-id="f60b4-127">Новый объект наследует все те же свойства.</span><span class="sxs-lookup"><span data-stu-id="f60b4-127">The new object inherits all of the same properties.</span></span> <span data-ttu-id="f60b4-128">В исходном объекте метод также разделяет любые эффекты, которые попадают в время разбиения.</span><span class="sxs-lookup"><span data-stu-id="f60b4-128">In a source object, the method also splits any effects that fall on the split time.</span></span>

<span data-ttu-id="f60b4-129">Вызов этого метода в дорожке разделяет все источники, эффекты и переходы, содержащиеся в дорожке, в указанное время разбиения.</span><span class="sxs-lookup"><span data-stu-id="f60b4-129">Calling this method on a track splits all the sources, effects, and transitions that are contained in the track at the specified split time.</span></span> <span data-ttu-id="f60b4-130">Вторая запись не создается. (Запись начинается в момент нулевого значения и расширяется на бесконечность.)</span><span class="sxs-lookup"><span data-stu-id="f60b4-130">It does not create a second track. (A track begins at time zero and extends to infinity.)</span></span>

<span data-ttu-id="f60b4-131">Для трассировки, если время разбиения позже, чем все в дорожке, метод возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="f60b4-131">For a track, if the split time is later than everything in the track, the method returns S\_FALSE.</span></span> <span data-ttu-id="f60b4-132">Для любого другого объекта, если время разбиения не попадает в объект, метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="f60b4-132">For any other object, if the split time does not fall anywhere within the object, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="f60b4-133">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f60b4-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f60b4-134">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f60b4-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f60b4-135">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f60b4-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f60b4-136">Требования</span><span class="sxs-lookup"><span data-stu-id="f60b4-136">Requirements</span></span>



| <span data-ttu-id="f60b4-137">Требование</span><span class="sxs-lookup"><span data-stu-id="f60b4-137">Requirement</span></span> | <span data-ttu-id="f60b4-138">Значение</span><span class="sxs-lookup"><span data-stu-id="f60b4-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f60b4-139">Header</span><span class="sxs-lookup"><span data-stu-id="f60b4-139">Header</span></span><br/>  | <dl> <span data-ttu-id="f60b4-140"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f60b4-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f60b4-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f60b4-141">Library</span></span><br/> | <dl> <span data-ttu-id="f60b4-142"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f60b4-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f60b4-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f60b4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f60b4-144">**Интерфейс Иамтимелинесплиттабле**</span><span class="sxs-lookup"><span data-stu-id="f60b4-144">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="f60b4-145">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f60b4-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




