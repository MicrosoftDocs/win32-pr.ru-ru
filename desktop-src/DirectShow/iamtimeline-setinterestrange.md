---
description: 'Метод Иамтимелине:: Сетинтерестранже не реализован.'
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: 'Метод Иамтимелине:: Сетинтерестранже (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInterestRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 23485bbdc2292e0d341e3fef0646fb68616698c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119572"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="c71da-103">Метод Иамтимелине:: Сетинтерестранже</span><span class="sxs-lookup"><span data-stu-id="c71da-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="c71da-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c71da-104">\[Deprecated.</span></span> <span data-ttu-id="c71da-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c71da-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c71da-106">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="c71da-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71da-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c71da-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="c71da-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c71da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71da-109">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="c71da-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="c71da-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c71da-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c71da-111">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="c71da-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="c71da-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c71da-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71da-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c71da-113">Return value</span></span>

<span data-ttu-id="c71da-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c71da-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c71da-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c71da-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c71da-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="c71da-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c71da-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c71da-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c71da-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c71da-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c71da-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c71da-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c71da-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c71da-120">Requirements</span></span>



| <span data-ttu-id="c71da-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c71da-121">Requirement</span></span> | <span data-ttu-id="c71da-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c71da-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c71da-123">Header</span><span class="sxs-lookup"><span data-stu-id="c71da-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c71da-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c71da-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c71da-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c71da-125">Library</span></span><br/> | <dl> <span data-ttu-id="c71da-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c71da-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c71da-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c71da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71da-128">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="c71da-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




