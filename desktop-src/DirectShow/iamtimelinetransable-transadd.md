---
description: Метод Трансадд добавляет переход к объекту. Объект может иметь несколько переходов, но они не должны перекрываться по времени. Переходы должны находиться в пределах временных границ объекта.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'Метод Иамтимелинетрансабле:: Трансадд (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689414"
---
# <a name="iamtimelinetransabletransadd-method"></a><span data-ttu-id="cb895-105">Метод Иамтимелинетрансабле:: Трансадд</span><span class="sxs-lookup"><span data-stu-id="cb895-105">IAMTimelineTransable::TransAdd method</span></span>

> [!Note]  
> <span data-ttu-id="cb895-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cb895-106">\[Deprecated.</span></span> <span data-ttu-id="cb895-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb895-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cb895-108">`TransAdd`Метод добавляет переход к объекту.</span><span class="sxs-lookup"><span data-stu-id="cb895-108">The `TransAdd` method adds a transition to the object.</span></span> <span data-ttu-id="cb895-109">Объект может иметь несколько переходов, но они не должны перекрываться по времени.</span><span class="sxs-lookup"><span data-stu-id="cb895-109">An object can have multiple transitions, but they must not overlap in time.</span></span> <span data-ttu-id="cb895-110">Переходы должны находиться в пределах временных границ объекта.</span><span class="sxs-lookup"><span data-stu-id="cb895-110">Transitions must fall within the time boundaries of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb895-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb895-111">Syntax</span></span>


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a><span data-ttu-id="cb895-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb895-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb895-113">*птранс*</span><span class="sxs-lookup"><span data-stu-id="cb895-113">*pTrans*</span></span> 
</dt> <dd>

<span data-ttu-id="cb895-114">Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) добавляемого перехода.</span><span class="sxs-lookup"><span data-stu-id="cb895-114">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the transition to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb895-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb895-115">Return value</span></span>

<span data-ttu-id="cb895-116">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="cb895-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="cb895-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cb895-117">Return code</span></span>                                                                                   | <span data-ttu-id="cb895-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cb895-118">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="cb895-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cb895-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cb895-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cb895-120">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cb895-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cb895-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cb895-122">Не удается вставить переход.</span><span class="sxs-lookup"><span data-stu-id="cb895-122">Cannot insert the transition.</span></span><br/>              |
| <dl> <span data-ttu-id="cb895-123"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="cb895-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="cb895-124">*птранс* не является указателем на переход.</span><span class="sxs-lookup"><span data-stu-id="cb895-124">*pTrans* is not a pointer to a transition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb895-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb895-125">Remarks</span></span>

<span data-ttu-id="cb895-126">Если переход перекрывает существующий переход, метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="cb895-126">If the transition overlaps an existing transition, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="cb895-127">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cb895-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cb895-128">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cb895-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cb895-129">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cb895-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb895-130">Требования</span><span class="sxs-lookup"><span data-stu-id="cb895-130">Requirements</span></span>



| <span data-ttu-id="cb895-131">Требование</span><span class="sxs-lookup"><span data-stu-id="cb895-131">Requirement</span></span> | <span data-ttu-id="cb895-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cb895-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb895-133">Header</span><span class="sxs-lookup"><span data-stu-id="cb895-133">Header</span></span><br/>  | <dl> <span data-ttu-id="cb895-134"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb895-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cb895-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb895-135">Library</span></span><br/> | <dl> <span data-ttu-id="cb895-136"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb895-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb895-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb895-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb895-138">**Интерфейс Иамтимелинетрансабле**</span><span class="sxs-lookup"><span data-stu-id="cb895-138">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="cb895-139">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="cb895-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




