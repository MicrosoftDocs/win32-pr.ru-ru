---
description: Метод Жетнексттранс извлекает первый переход, который отображается в указанное время или позже.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Метод Иамтимелинетрансабле:: Жетнексттранс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685047"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a><span data-ttu-id="a70f6-103">Метод Иамтимелинетрансабле:: Жетнексттранс</span><span class="sxs-lookup"><span data-stu-id="a70f6-103">IAMTimelineTransable::GetNextTrans method</span></span>

> [!Note]  
> <span data-ttu-id="a70f6-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a70f6-104">\[Deprecated.</span></span> <span data-ttu-id="a70f6-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a70f6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a70f6-106">`GetNextTrans`Метод извлекает первый переход, который отображается в указанное время или позже.</span><span class="sxs-lookup"><span data-stu-id="a70f6-106">The `GetNextTrans` method retrieves the first transition that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a70f6-107">Syntax</span></span>


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="a70f6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a70f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a70f6-109">*пптранс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a70f6-109">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a70f6-110">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) объекта перехода.</span><span class="sxs-lookup"><span data-stu-id="a70f6-110">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a70f6-111">*\Sub*</span><span class="sxs-lookup"><span data-stu-id="a70f6-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="a70f6-112">Указатель на переменную, указывающую время в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="a70f6-112">Pointer to a variable that specifies the time in 100-nanosecond units.</span></span> <span data-ttu-id="a70f6-113">В поле входное значение указывает время, с которого нужно найти переход.</span><span class="sxs-lookup"><span data-stu-id="a70f6-113">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="a70f6-114">В выходных данных, если переход получен, это значение устанавливается равным времени окончания перехода.</span><span class="sxs-lookup"><span data-stu-id="a70f6-114">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a70f6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a70f6-115">Return value</span></span>

<span data-ttu-id="a70f6-116">Возвращает \_ ОК, если метод получает переход, или \_ значение false, если не удается найти переход.</span><span class="sxs-lookup"><span data-stu-id="a70f6-116">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="a70f6-117">В противном случае возвращает значение **HRESULT** , указывающее причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="a70f6-117">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a70f6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a70f6-118">Remarks</span></span>

<span data-ttu-id="a70f6-119">Время начала перехода может быть меньше времени, указанного в *схеме контактов*, если переход охватывает указанное время.</span><span class="sxs-lookup"><span data-stu-id="a70f6-119">The start time of the transition might be less than the time that you specify in *pInOut*, if the transition spans the specified time.</span></span>

<span data-ttu-id="a70f6-120">Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс [**иамтимелинеобж**](iamtimelineobj.md) имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="a70f6-120">If the method returns S\_OK, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="a70f6-121">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="a70f6-121">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="a70f6-122">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a70f6-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a70f6-123">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a70f6-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a70f6-124">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a70f6-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a70f6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a70f6-125">Requirements</span></span>



| <span data-ttu-id="a70f6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a70f6-126">Requirement</span></span> | <span data-ttu-id="a70f6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a70f6-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70f6-128">Header</span><span class="sxs-lookup"><span data-stu-id="a70f6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a70f6-129"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a70f6-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a70f6-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a70f6-130">Library</span></span><br/> | <dl> <span data-ttu-id="a70f6-131"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a70f6-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a70f6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a70f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70f6-133">**Интерфейс Иамтимелинетрансабле**</span><span class="sxs-lookup"><span data-stu-id="a70f6-133">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="a70f6-134">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a70f6-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




