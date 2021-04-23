---
description: Метод Инсертспаце разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'Метод Иамтимелинетракк:: Инсертспаце (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685236"
---
# <a name="iamtimelinetrackinsertspace-method"></a><span data-ttu-id="e734f-103">Метод Иамтимелинетракк:: Инсертспаце</span><span class="sxs-lookup"><span data-stu-id="e734f-103">IAMTimelineTrack::InsertSpace method</span></span>

> [!Note]  
> <span data-ttu-id="e734f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e734f-104">\[Deprecated.</span></span> <span data-ttu-id="e734f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e734f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e734f-106">`InsertSpace`Метод разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы.</span><span class="sxs-lookup"><span data-stu-id="e734f-106">The `InsertSpace` method splits any objects that exist at the specified time and inserts space between them.</span></span>

## <a name="syntax"></a><span data-ttu-id="e734f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e734f-107">Syntax</span></span>


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="e734f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e734f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e734f-109">*ртстарт*</span><span class="sxs-lookup"><span data-stu-id="e734f-109">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="e734f-110">Время, когда нужно создать разбиение, и начальную точку вставленного пространства в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="e734f-110">Time at which to create the split, and the starting point of the inserted space, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e734f-111">*ртенд*</span><span class="sxs-lookup"><span data-stu-id="e734f-111">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e734f-112">Конечная точка вставленного пространства в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="e734f-112">End point of the inserted space, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e734f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e734f-113">Return value</span></span>

<span data-ttu-id="e734f-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e734f-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e734f-115">Возможные возвращаемые значения включают следующее.</span><span class="sxs-lookup"><span data-stu-id="e734f-115">Possible return values include the following:</span></span>



| <span data-ttu-id="e734f-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e734f-116">Return code</span></span>                                                                                   | <span data-ttu-id="e734f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e734f-117">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="e734f-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e734f-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="e734f-119">В указанное время нет объектов.</span><span class="sxs-lookup"><span data-stu-id="e734f-119">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="e734f-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e734f-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e734f-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e734f-121">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e734f-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e734f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e734f-123">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="e734f-123">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="e734f-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e734f-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e734f-125">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="e734f-125">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="e734f-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e734f-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e734f-127">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="e734f-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e734f-128">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e734f-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e734f-129">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e734f-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e734f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e734f-130">Requirements</span></span>



| <span data-ttu-id="e734f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e734f-131">Requirement</span></span> | <span data-ttu-id="e734f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e734f-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e734f-133">Header</span><span class="sxs-lookup"><span data-stu-id="e734f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e734f-134"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="e734f-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e734f-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e734f-135">Library</span></span><br/> | <dl> <span data-ttu-id="e734f-136"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e734f-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e734f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e734f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e734f-138">**Интерфейс Иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="e734f-138">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="e734f-139">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="e734f-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




