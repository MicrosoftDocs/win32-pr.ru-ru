---
description: 'Метод ModifyStopTime2 задает время окончания. Этот метод эквивалентен Иамтимелинесрк:: Модифистоптиме, но принимает значение РЕФТИМЕ.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Метод Иамтимелинесрк:: ModifyStopTime2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689360"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a><span data-ttu-id="f9113-104">Метод Иамтимелинесрк:: ModifyStopTime2</span><span class="sxs-lookup"><span data-stu-id="f9113-104">IAMTimelineSrc::ModifyStopTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="f9113-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f9113-105">\[Deprecated.</span></span> <span data-ttu-id="f9113-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9113-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f9113-107">`ModifyStopTime2`Метод задает время окончания.</span><span class="sxs-lookup"><span data-stu-id="f9113-107">The `ModifyStopTime2` method sets the stop time.</span></span> <span data-ttu-id="f9113-108">Этот метод эквивалентен [**иамтимелинесрк:: модифистоптиме**](iamtimelinesrc-modifystoptime.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="f9113-108">This method is equivalent to [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9113-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9113-109">Syntax</span></span>


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="f9113-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9113-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9113-111">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="f9113-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="f9113-112">Новое время окончания в секундах.</span><span class="sxs-lookup"><span data-stu-id="f9113-112">New stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9113-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9113-113">Return value</span></span>

<span data-ttu-id="f9113-114">Возвращает значение \_ ОК, если успешно, или E \_ INVALIDARG, если указанное время недопустимо.</span><span class="sxs-lookup"><span data-stu-id="f9113-114">Returns S\_OK if successful, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9113-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9113-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9113-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f9113-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9113-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f9113-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f9113-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f9113-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9113-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f9113-119">Requirements</span></span>



| <span data-ttu-id="f9113-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f9113-120">Requirement</span></span> | <span data-ttu-id="f9113-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f9113-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9113-122">Header</span><span class="sxs-lookup"><span data-stu-id="f9113-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f9113-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9113-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f9113-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f9113-124">Library</span></span><br/> | <dl> <span data-ttu-id="f9113-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9113-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9113-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9113-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9113-127">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="f9113-127">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="f9113-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f9113-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




