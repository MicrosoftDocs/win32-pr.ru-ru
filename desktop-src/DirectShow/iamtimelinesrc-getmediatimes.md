---
description: Метод Жетмедиатимес получает время начала и окончания воспроизведения носителя.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'Метод Иамтимелинесрк:: Жетмедиатимес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689369"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a><span data-ttu-id="d7b36-103">Метод Иамтимелинесрк:: Жетмедиатимес</span><span class="sxs-lookup"><span data-stu-id="d7b36-103">IAMTimelineSrc::GetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="d7b36-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d7b36-104">\[Deprecated.</span></span> <span data-ttu-id="d7b36-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7b36-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d7b36-106">`GetMediaTimes`Метод получает время начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="d7b36-106">The `GetMediaTimes` method retrieves the media start and stop times.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b36-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b36-107">Syntax</span></span>


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="d7b36-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7b36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b36-109">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="d7b36-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b36-110">Получает время начала носителя в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="d7b36-110">Receives the media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="d7b36-111">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="d7b36-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b36-112">Получает время окончания передачи мультимедиа в единицах с 100 нс.</span><span class="sxs-lookup"><span data-stu-id="d7b36-112">Receives the media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b36-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7b36-113">Return value</span></span>

<span data-ttu-id="d7b36-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d7b36-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7b36-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7b36-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7b36-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7b36-116">Remarks</span></span>

<span data-ttu-id="d7b36-117">Время носителя задается относительно исходного файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d7b36-117">The media times are relative to the original media file.</span></span> <span data-ttu-id="d7b36-118">Дополнительные сведения см. [в разделе время в службах редактирования DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="d7b36-118">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="d7b36-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d7b36-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d7b36-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7b36-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d7b36-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d7b36-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7b36-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d7b36-122">Requirements</span></span>



| <span data-ttu-id="d7b36-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d7b36-123">Requirement</span></span> | <span data-ttu-id="d7b36-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b36-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b36-125">Header</span><span class="sxs-lookup"><span data-stu-id="d7b36-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d7b36-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7b36-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d7b36-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7b36-127">Library</span></span><br/> | <dl> <span data-ttu-id="d7b36-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7b36-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b36-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7b36-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b36-130">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="d7b36-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d7b36-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d7b36-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




