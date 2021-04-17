---
description: 'Не поддерживается. Вместо этого вызовите метод Иамтимелинекомп:: Жетрекурсивелайерофтипе.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'Метод Иамтимелинекомп:: Жетрекурсивелайерофтипеи (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685344"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a><span data-ttu-id="198fa-104">Метод Иамтимелинекомп:: Жетрекурсивелайерофтипеи</span><span class="sxs-lookup"><span data-stu-id="198fa-104">IAMTimelineComp::GetRecursiveLayerOfTypeI method</span></span>

> [!Note]  
> <span data-ttu-id="198fa-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="198fa-105">\[Deprecated.</span></span> <span data-ttu-id="198fa-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="198fa-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="198fa-107">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="198fa-107">Not supported.</span></span> <span data-ttu-id="198fa-108">Вместо этого вызовите метод [**иамтимелинекомп:: жетрекурсивелайерофтипе**](iamtimelinecomp-getrecursivelayeroftype.md) .</span><span class="sxs-lookup"><span data-stu-id="198fa-108">Call the [**IAMTimelineComp::GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="198fa-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="198fa-109">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="198fa-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="198fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198fa-111">*ппвиртуалтракк*</span><span class="sxs-lookup"><span data-stu-id="198fa-111">*ppVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="198fa-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="198fa-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="198fa-113">*пвхичлайер*</span><span class="sxs-lookup"><span data-stu-id="198fa-113">*pWhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="198fa-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="198fa-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="198fa-115">*Тип*</span><span class="sxs-lookup"><span data-stu-id="198fa-115">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="198fa-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="198fa-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198fa-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="198fa-117">Return value</span></span>

<span data-ttu-id="198fa-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="198fa-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="198fa-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="198fa-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="198fa-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="198fa-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="198fa-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="198fa-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="198fa-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="198fa-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="198fa-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="198fa-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="198fa-124">Требования</span><span class="sxs-lookup"><span data-stu-id="198fa-124">Requirements</span></span>



| <span data-ttu-id="198fa-125">Требование</span><span class="sxs-lookup"><span data-stu-id="198fa-125">Requirement</span></span> | <span data-ttu-id="198fa-126">Значение</span><span class="sxs-lookup"><span data-stu-id="198fa-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="198fa-127">Header</span><span class="sxs-lookup"><span data-stu-id="198fa-127">Header</span></span><br/>  | <dl> <span data-ttu-id="198fa-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="198fa-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="198fa-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="198fa-129">Library</span></span><br/> | <dl> <span data-ttu-id="198fa-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="198fa-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="198fa-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="198fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198fa-132">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="198fa-132">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> </dl>

 

 




