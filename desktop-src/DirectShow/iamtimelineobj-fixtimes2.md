---
description: 'Метод FixTimes2 Округляет указанное время начала и окончания до ближайших границ фрейма, как определено параметром частоты кадров родительской группы. Этот метод эквивалентен Иамтимелинеобж:: Фикстимес, но принимает значения РЕФТИМЕ.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'Метод Иамтимелинеобж:: FixTimes2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680040"
---
# <a name="iamtimelineobjfixtimes2-method"></a><span data-ttu-id="5c971-104">Метод Иамтимелинеобж:: FixTimes2</span><span class="sxs-lookup"><span data-stu-id="5c971-104">IAMTimelineObj::FixTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="5c971-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5c971-105">\[Deprecated.</span></span> <span data-ttu-id="5c971-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5c971-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5c971-107">`FixTimes2`Метод Округляет указанное время начала и окончания до ближайших границ фрейма, как определено параметром частоты кадров родительской группы.</span><span class="sxs-lookup"><span data-stu-id="5c971-107">The `FixTimes2` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span> <span data-ttu-id="5c971-108">Этот метод эквивалентен [**иамтимелинеобж:: фикстимес**](iamtimelineobj-fixtimes.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="5c971-108">This method is equivalent to [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c971-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c971-109">Syntax</span></span>


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="5c971-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c971-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c971-111">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="5c971-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="5c971-112">Указатель на переменную, содержащую время начала в секундах.</span><span class="sxs-lookup"><span data-stu-id="5c971-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="5c971-113">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="5c971-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="5c971-114">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="5c971-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="5c971-115">Указатель на переменную, содержащую время окончания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="5c971-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="5c971-116">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="5c971-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c971-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c971-117">Return value</span></span>

<span data-ttu-id="5c971-118">Возвращает \_ ОК в случае успеха или E \_ нотинтри, если объект не является частью группы.</span><span class="sxs-lookup"><span data-stu-id="5c971-118">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c971-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c971-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5c971-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5c971-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5c971-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5c971-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5c971-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5c971-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c971-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5c971-123">Requirements</span></span>



| <span data-ttu-id="5c971-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5c971-124">Requirement</span></span> | <span data-ttu-id="5c971-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5c971-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c971-126">Header</span><span class="sxs-lookup"><span data-stu-id="5c971-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5c971-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c971-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5c971-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c971-128">Library</span></span><br/> | <dl> <span data-ttu-id="5c971-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c971-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c971-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c971-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c971-131">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="5c971-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5c971-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5c971-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




