---
description: 'Метод InsertSpace2 разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы. Этот метод эквивалентен Иамтимелинетракк:: Инсертспаце, но принимает значения РЕФТИМЕ.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'Метод Иамтимелинетракк:: InsertSpace2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685232"
---
# <a name="iamtimelinetrackinsertspace2-method"></a><span data-ttu-id="2ece3-104">Метод Иамтимелинетракк:: InsertSpace2</span><span class="sxs-lookup"><span data-stu-id="2ece3-104">IAMTimelineTrack::InsertSpace2 method</span></span>

> [!Note]  
> <span data-ttu-id="2ece3-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2ece3-105">\[Deprecated.</span></span> <span data-ttu-id="2ece3-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2ece3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2ece3-107">`InsertSpace2`Метод разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы.</span><span class="sxs-lookup"><span data-stu-id="2ece3-107">The `InsertSpace2` method splits any objects that exist at the specified time and inserts space between them.</span></span> <span data-ttu-id="2ece3-108">Этот метод эквивалентен [**иамтимелинетракк:: инсертспаце**](iamtimelinetrack-insertspace.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="2ece3-108">This method is equivalent to [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ece3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ece3-109">Syntax</span></span>


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="2ece3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ece3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ece3-111">*ртстарт*</span><span class="sxs-lookup"><span data-stu-id="2ece3-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="2ece3-112">Время, когда нужно создать разбиение, и начальную точку вставленного пространства в секундах.</span><span class="sxs-lookup"><span data-stu-id="2ece3-112">Time at which to create the split, and the starting point of the inserted space, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="2ece3-113">*ртенд*</span><span class="sxs-lookup"><span data-stu-id="2ece3-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2ece3-114">Конечная точка вставленного пространства в секундах.</span><span class="sxs-lookup"><span data-stu-id="2ece3-114">End point of the inserted space, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ece3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ece3-115">Return value</span></span>

<span data-ttu-id="2ece3-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ece3-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2ece3-117">Возможные возвращаемые значения включают следующее.</span><span class="sxs-lookup"><span data-stu-id="2ece3-117">Possible return values include the following:</span></span>



| <span data-ttu-id="2ece3-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2ece3-118">Return code</span></span>                                                                                   | <span data-ttu-id="2ece3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="2ece3-119">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="2ece3-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2ece3-120"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="2ece3-121">В указанное время нет объектов.</span><span class="sxs-lookup"><span data-stu-id="2ece3-121">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="2ece3-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2ece3-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ece3-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2ece3-123">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2ece3-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2ece3-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2ece3-125">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="2ece3-125">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="2ece3-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2ece3-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2ece3-127">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="2ece3-127">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="2ece3-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ece3-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2ece3-129">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2ece3-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2ece3-130">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2ece3-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2ece3-131">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2ece3-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ece3-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2ece3-132">Requirements</span></span>



| <span data-ttu-id="2ece3-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2ece3-133">Requirement</span></span> | <span data-ttu-id="2ece3-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2ece3-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ece3-135">Header</span><span class="sxs-lookup"><span data-stu-id="2ece3-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2ece3-136"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ece3-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2ece3-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ece3-137">Library</span></span><br/> | <dl> <span data-ttu-id="2ece3-138"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ece3-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ece3-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ece3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ece3-140">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="2ece3-140">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="2ece3-141">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="2ece3-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




