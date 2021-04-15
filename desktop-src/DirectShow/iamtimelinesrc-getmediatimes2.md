---
description: 'Метод GetMediaTimes2 получает время начала и окончания воспроизведения носителя. Этот метод эквивалентен Иамтимелинесрк:: Жетмедиатимес, но принимает значения РЕФТИМЕ.'
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'Метод Иамтимелинесрк:: GetMediaTimes2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675886"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a><span data-ttu-id="34c07-104">Метод Иамтимелинесрк:: GetMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="34c07-104">IAMTimelineSrc::GetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="34c07-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="34c07-105">\[Deprecated.</span></span> <span data-ttu-id="34c07-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="34c07-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="34c07-107">`GetMediaTimes2`Метод получает время начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="34c07-107">The `GetMediaTimes2` method retrieves the media start and stop times.</span></span> <span data-ttu-id="34c07-108">Этот метод эквивалентен [**иамтимелинесрк:: жетмедиатимес**](iamtimelinesrc-getmediatimes.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="34c07-108">This method is equivalent to [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="34c07-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34c07-109">Syntax</span></span>


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="34c07-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="34c07-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34c07-111">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="34c07-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="34c07-112">Получает время начала воспроизведения в секундах.</span><span class="sxs-lookup"><span data-stu-id="34c07-112">Receives the media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="34c07-113">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="34c07-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="34c07-114">Получает время окончания воспроизведения в секундах.</span><span class="sxs-lookup"><span data-stu-id="34c07-114">Receives the media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34c07-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34c07-115">Return value</span></span>

<span data-ttu-id="34c07-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="34c07-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34c07-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34c07-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="34c07-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34c07-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="34c07-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="34c07-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="34c07-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="34c07-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="34c07-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="34c07-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34c07-122">Требования</span><span class="sxs-lookup"><span data-stu-id="34c07-122">Requirements</span></span>



| <span data-ttu-id="34c07-123">Требование</span><span class="sxs-lookup"><span data-stu-id="34c07-123">Requirement</span></span> | <span data-ttu-id="34c07-124">Значение</span><span class="sxs-lookup"><span data-stu-id="34c07-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34c07-125">Header</span><span class="sxs-lookup"><span data-stu-id="34c07-125">Header</span></span><br/>  | <dl> <span data-ttu-id="34c07-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="34c07-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="34c07-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34c07-127">Library</span></span><br/> | <dl> <span data-ttu-id="34c07-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34c07-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c07-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34c07-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c07-130">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="34c07-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="34c07-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="34c07-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




