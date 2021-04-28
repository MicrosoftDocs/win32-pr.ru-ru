---
description: 'Метод Иамтимелине:: Ремграупфромлист не поддерживается.'
ms.assetid: 9ad5f5ee-2a2a-448b-9da4-2ad8d543eb22
title: 'Метод Иамтимелине:: Ремграупфромлист (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.RemGroupFromList
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fcb2a73f32ab1c1f401a4508c63e53cc58ebcfb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098692"
---
# <a name="iamtimelineremgroupfromlist-method"></a><span data-ttu-id="9b4e0-103">Метод Иамтимелине:: Ремграупфромлист</span><span class="sxs-lookup"><span data-stu-id="9b4e0-103">IAMTimeline::RemGroupFromList method</span></span>

> [!Note]  
> <span data-ttu-id="9b4e0-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-104">\[Deprecated.</span></span> <span data-ttu-id="9b4e0-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9b4e0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9b4e0-106">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4e0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b4e0-107">Syntax</span></span>


```C++
HRESULT RemGroupFromList(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="9b4e0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b4e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4e0-109">*пграуп*</span><span class="sxs-lookup"><span data-stu-id="9b4e0-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4e0-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b4e0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b4e0-111">Return value</span></span>

<span data-ttu-id="9b4e0-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b4e0-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b4e0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b4e0-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b4e0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9b4e0-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9b4e0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9b4e0-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b4e0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9b4e0-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9b4e0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b4e0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9b4e0-118">Requirements</span></span>



| <span data-ttu-id="9b4e0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9b4e0-119">Requirement</span></span> | <span data-ttu-id="9b4e0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9b4e0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4e0-121">Header</span><span class="sxs-lookup"><span data-stu-id="9b4e0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9b4e0-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b4e0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9b4e0-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b4e0-123">Library</span></span><br/> | <dl> <span data-ttu-id="9b4e0-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b4e0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b4e0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="9b4e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4e0-126">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="9b4e0-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




