---
description: 'Метод GetNextTrans2 извлекает первый переход, который отображается в указанное время или позже. Этот метод эквивалентен Иамтимелинетрансабле:: Жетнексттранс, но принимает значение РЕФТИМЕ.'
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'Метод Иамтимелинетрансабле:: GetNextTrans2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689419"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a><span data-ttu-id="a0047-104">Метод Иамтимелинетрансабле:: GetNextTrans2</span><span class="sxs-lookup"><span data-stu-id="a0047-104">IAMTimelineTransable::GetNextTrans2 method</span></span>

> [!Note]  
> <span data-ttu-id="a0047-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a0047-105">\[Deprecated.</span></span> <span data-ttu-id="a0047-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0047-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a0047-107">`GetNextTrans2`Метод извлекает первый переход, который отображается в указанное время или позже.</span><span class="sxs-lookup"><span data-stu-id="a0047-107">The `GetNextTrans2` method retrieves the first transition that appears at the specified time or later.</span></span> <span data-ttu-id="a0047-108">Этот метод эквивалентен [**иамтимелинетрансабле:: жетнексттранс**](iamtimelinetransable-getnexttrans.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="a0047-108">This method is equivalent to [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0047-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0047-109">Syntax</span></span>


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="a0047-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0047-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0047-111">*пптранс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a0047-111">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0047-112">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) объекта перехода.</span><span class="sxs-lookup"><span data-stu-id="a0047-112">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a0047-113">*\Sub*</span><span class="sxs-lookup"><span data-stu-id="a0047-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="a0047-114">Указатель на переменную, указывающую время в секундах.</span><span class="sxs-lookup"><span data-stu-id="a0047-114">Pointer to a variable that specifies the time in seconds.</span></span> <span data-ttu-id="a0047-115">В поле входное значение указывает время, с которого нужно найти переход.</span><span class="sxs-lookup"><span data-stu-id="a0047-115">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="a0047-116">В выходных данных, если переход получен, это значение устанавливается равным времени окончания перехода.</span><span class="sxs-lookup"><span data-stu-id="a0047-116">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0047-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0047-117">Return value</span></span>

<span data-ttu-id="a0047-118">Возвращает \_ ОК, если метод получает переход, или \_ значение false, если не удается найти переход.</span><span class="sxs-lookup"><span data-stu-id="a0047-118">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="a0047-119">В противном случае возвращает значение **HRESULT** , указывающее причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="a0047-119">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0047-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0047-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a0047-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a0047-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a0047-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0047-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a0047-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a0047-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0047-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a0047-124">Requirements</span></span>



| <span data-ttu-id="a0047-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a0047-125">Requirement</span></span> | <span data-ttu-id="a0047-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a0047-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0047-127">Header</span><span class="sxs-lookup"><span data-stu-id="a0047-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a0047-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0047-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a0047-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0047-129">Library</span></span><br/> | <dl> <span data-ttu-id="a0047-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0047-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0047-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0047-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0047-132">**Интерфейс Иамтимелинетрансабле**</span><span class="sxs-lookup"><span data-stu-id="a0047-132">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="a0047-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a0047-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




