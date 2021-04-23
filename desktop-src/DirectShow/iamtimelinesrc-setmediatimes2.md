---
description: 'Метод SetMediaTimes2 задает время начала и окончания воспроизведения носителя. Этот метод эквивалентен Иамтимелинесрк:: Сетмедиатимес, но принимает значения РЕФТИМЕ.'
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'Метод Иамтимелинесрк:: SetMediaTimes2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689357"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a><span data-ttu-id="d5942-104">Метод Иамтимелинесрк:: SetMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="d5942-104">IAMTimelineSrc::SetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="d5942-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d5942-105">\[Deprecated.</span></span> <span data-ttu-id="d5942-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d5942-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d5942-107">`SetMediaTimes2`Метод задает время начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="d5942-107">The `SetMediaTimes2` method sets the media stop and start times.</span></span> <span data-ttu-id="d5942-108">Этот метод эквивалентен [**иамтимелинесрк:: сетмедиатимес**](iamtimelinesrc-setmediatimes.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="d5942-108">This method is equivalent to [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5942-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5942-109">Syntax</span></span>


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="d5942-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5942-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5942-111">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="d5942-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="d5942-112">Время запуска носителя в секундах.</span><span class="sxs-lookup"><span data-stu-id="d5942-112">Media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d5942-113">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="d5942-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="d5942-114">Время окончания носителя в секундах.</span><span class="sxs-lookup"><span data-stu-id="d5942-114">Media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5942-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5942-115">Return value</span></span>

<span data-ttu-id="d5942-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d5942-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5942-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5942-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5942-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5942-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5942-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d5942-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d5942-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5942-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d5942-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d5942-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5942-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d5942-122">Requirements</span></span>



| <span data-ttu-id="d5942-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d5942-123">Requirement</span></span> | <span data-ttu-id="d5942-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d5942-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5942-125">Header</span><span class="sxs-lookup"><span data-stu-id="d5942-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d5942-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5942-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d5942-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5942-127">Library</span></span><br/> | <dl> <span data-ttu-id="d5942-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5942-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5942-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5942-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5942-130">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="d5942-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d5942-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d5942-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




