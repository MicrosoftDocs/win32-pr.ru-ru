---
description: Метод Еффектинсбефоре вставляет результат в объект с указанным уровнем приоритета.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Метод Иамтимелиниффектабле:: Еффектинсбефоре (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680071"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a><span data-ttu-id="49248-103">Метод Иамтимелиниффектабле:: Еффектинсбефоре</span><span class="sxs-lookup"><span data-stu-id="49248-103">IAMTimelineEffectable::EffectInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="49248-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="49248-104">\[Deprecated.</span></span> <span data-ttu-id="49248-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49248-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="49248-106">`EffectInsBefore`Метод вставляет результат в объект с указанным уровнем приоритета.</span><span class="sxs-lookup"><span data-stu-id="49248-106">The `EffectInsBefore` method inserts an effect into the object at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="49248-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49248-107">Syntax</span></span>


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="49248-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49248-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49248-109">*Сохраняется*</span><span class="sxs-lookup"><span data-stu-id="49248-109">*pFX*</span></span> 
</dt> <dd>

<span data-ttu-id="49248-110">Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) этого действия.</span><span class="sxs-lookup"><span data-stu-id="49248-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="49248-111">*Приоритет*</span><span class="sxs-lookup"><span data-stu-id="49248-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="49248-112">Уровень приоритета, на который следует вставить результат.</span><span class="sxs-lookup"><span data-stu-id="49248-112">Priority level at which to insert the effect.</span></span> <span data-ttu-id="49248-113">Чтобы вставить результат в конец списка приоритетов, используйте значение-1.</span><span class="sxs-lookup"><span data-stu-id="49248-113">Use the value –1 to insert the effect at the end of the priority list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49248-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49248-114">Return value</span></span>

<span data-ttu-id="49248-115">При \_ успешном выполнении или E нотимпл возвращает значение ОК, \_ Если объект не является результатом.</span><span class="sxs-lookup"><span data-stu-id="49248-115">Returns S\_OK if successful or E\_NOTIMPL if the object is not an effect.</span></span> <span data-ttu-id="49248-116">В противном случае возвращает другое значение **HRESULT** , указывающее причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="49248-116">Otherwise, returns another **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="49248-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49248-117">Remarks</span></span>

<span data-ttu-id="49248-118">Время начала и окончания действия обрезается в пределах диапазона времени объекта, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="49248-118">The start and stop times of the effect are clipped within the bounds of the object's time range, if necessary.</span></span> <span data-ttu-id="49248-119">Если на указанном уровне приоритета уже действует, все эффекты, произведенные с этого момента, перемещаются вниз по списку приоритетов, чтобы освободить место для нового эффекта.</span><span class="sxs-lookup"><span data-stu-id="49248-119">If there is already an effect at the specified priority level, all the effects from that point on move down the priority list to make room for the new effect.</span></span>

> [!Note]  
> <span data-ttu-id="49248-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="49248-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="49248-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="49248-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="49248-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="49248-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49248-123">Требования</span><span class="sxs-lookup"><span data-stu-id="49248-123">Requirements</span></span>



| <span data-ttu-id="49248-124">Требование</span><span class="sxs-lookup"><span data-stu-id="49248-124">Requirement</span></span> | <span data-ttu-id="49248-125">Значение</span><span class="sxs-lookup"><span data-stu-id="49248-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49248-126">Header</span><span class="sxs-lookup"><span data-stu-id="49248-126">Header</span></span><br/>  | <dl> <span data-ttu-id="49248-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="49248-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="49248-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49248-128">Library</span></span><br/> | <dl> <span data-ttu-id="49248-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49248-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49248-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49248-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49248-131">**Интерфейс Иамтимелиниффектабле**</span><span class="sxs-lookup"><span data-stu-id="49248-131">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="49248-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="49248-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




