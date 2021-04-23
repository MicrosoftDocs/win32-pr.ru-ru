---
description: Метод Еффектсвапприоритиес переключает уровни приоритета двух эффектов.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'Метод Иамтимелиниффектабле:: Еффектсвапприоритиес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689500"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a><span data-ttu-id="cfd64-103">Метод Иамтимелиниффектабле:: Еффектсвапприоритиес</span><span class="sxs-lookup"><span data-stu-id="cfd64-103">IAMTimelineEffectable::EffectSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="cfd64-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cfd64-104">\[Deprecated.</span></span> <span data-ttu-id="cfd64-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cfd64-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cfd64-106">`EffectSwapPriorities`Метод переключает уровни приоритета двух эффектов.</span><span class="sxs-lookup"><span data-stu-id="cfd64-106">The `EffectSwapPriorities` method switches the priority levels of two effects.</span></span>

<span data-ttu-id="cfd64-107">При наличии двух значений приоритета этот метод меняет местами эти приоритеты.</span><span class="sxs-lookup"><span data-stu-id="cfd64-107">Given two priority values, this method swaps the effects at those priorities.</span></span> <span data-ttu-id="cfd64-108">При возврате из метода результат, который был на первом уровне приоритета, находится на втором уровне приоритета, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="cfd64-108">When the method returns, the effect that was at the first priority level is at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd64-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfd64-109">Syntax</span></span>


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a><span data-ttu-id="cfd64-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfd64-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd64-111">*Приоритет*</span><span class="sxs-lookup"><span data-stu-id="cfd64-111">*PriorityA*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd64-112">Первый уровень приоритета для переключения эффектов.</span><span class="sxs-lookup"><span data-stu-id="cfd64-112">First priority level at which to swap effects.</span></span>

</dd> <dt>

<span data-ttu-id="cfd64-113">*приоритиб*</span><span class="sxs-lookup"><span data-stu-id="cfd64-113">*PriorityB*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd64-114">Второй уровень приоритета для переключения эффектов.</span><span class="sxs-lookup"><span data-stu-id="cfd64-114">Second priority level at which to swap effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd64-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfd64-115">Return value</span></span>

<span data-ttu-id="cfd64-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cfd64-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cfd64-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cfd64-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfd64-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfd64-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cfd64-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cfd64-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cfd64-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfd64-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cfd64-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cfd64-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfd64-122">Требования</span><span class="sxs-lookup"><span data-stu-id="cfd64-122">Requirements</span></span>



| <span data-ttu-id="cfd64-123">Требование</span><span class="sxs-lookup"><span data-stu-id="cfd64-123">Requirement</span></span> | <span data-ttu-id="cfd64-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cfd64-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd64-125">Header</span><span class="sxs-lookup"><span data-stu-id="cfd64-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cfd64-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfd64-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cfd64-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cfd64-127">Library</span></span><br/> | <dl> <span data-ttu-id="cfd64-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfd64-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd64-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfd64-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd64-130">**Интерфейс Иамтимелиниффектабле**</span><span class="sxs-lookup"><span data-stu-id="cfd64-130">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="cfd64-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="cfd64-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




