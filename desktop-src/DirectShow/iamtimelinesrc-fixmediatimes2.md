---
description: 'Метод FixMediaTimes2 округляет указанные значения времени до ближайшей границы фрейма, как определено частотой выходного кадра. Этот метод эквивалентен Иамтимелинесрк:: Фиксмедиатимес, но принимает значения РЕФТИМЕ.'
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'Метод Иамтимелинесрк:: FixMediaTimes2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685082"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a><span data-ttu-id="05a77-104">Метод Иамтимелинесрк:: FixMediaTimes2</span><span class="sxs-lookup"><span data-stu-id="05a77-104">IAMTimelineSrc::FixMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="05a77-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="05a77-105">\[Deprecated.</span></span> <span data-ttu-id="05a77-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05a77-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="05a77-107">`FixMediaTimes2`Метод округляет указанные значения времени до ближайшей границы фрейма, как определено частотой выходного кадра.</span><span class="sxs-lookup"><span data-stu-id="05a77-107">The `FixMediaTimes2` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="05a77-108">Этот метод эквивалентен [**иамтимелинесрк:: фиксмедиатимес**](iamtimelinesrc-fixmediatimes.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="05a77-108">This method is equivalent to [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a77-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05a77-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="05a77-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="05a77-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a77-111">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="05a77-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="05a77-112">Указатель на переменную, содержащую время начала в секундах.</span><span class="sxs-lookup"><span data-stu-id="05a77-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="05a77-113">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="05a77-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="05a77-114">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="05a77-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="05a77-115">Указатель на переменную, содержащую время окончания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="05a77-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="05a77-116">Если вызов будет выполнен, для этой переменной задается округленное время.</span><span class="sxs-lookup"><span data-stu-id="05a77-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a77-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05a77-117">Return value</span></span>

<span data-ttu-id="05a77-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="05a77-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05a77-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05a77-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="05a77-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05a77-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05a77-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="05a77-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="05a77-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="05a77-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05a77-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="05a77-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05a77-124">Требования</span><span class="sxs-lookup"><span data-stu-id="05a77-124">Requirements</span></span>



| <span data-ttu-id="05a77-125">Требование</span><span class="sxs-lookup"><span data-stu-id="05a77-125">Requirement</span></span> | <span data-ttu-id="05a77-126">Значение</span><span class="sxs-lookup"><span data-stu-id="05a77-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05a77-127">Header</span><span class="sxs-lookup"><span data-stu-id="05a77-127">Header</span></span><br/>  | <dl> <span data-ttu-id="05a77-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="05a77-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="05a77-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05a77-129">Library</span></span><br/> | <dl> <span data-ttu-id="05a77-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05a77-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a77-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05a77-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a77-132">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="05a77-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="05a77-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="05a77-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




