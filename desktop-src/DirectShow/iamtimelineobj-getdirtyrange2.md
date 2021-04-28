---
description: 'Метод Иамтимелинеобж:: GetDirtyRange2 не поддерживается.'
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: 'Метод Иамтимелинеобж:: GetDirtyRange2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 14c573403bf946b54bbfcc74ae41145a3f1c5c7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119522"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a><span data-ttu-id="7ffcc-103">Метод Иамтимелинеобж:: GetDirtyRange2</span><span class="sxs-lookup"><span data-stu-id="7ffcc-103">IAMTimelineObj::GetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="7ffcc-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7ffcc-104">\[Deprecated.</span></span> <span data-ttu-id="7ffcc-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ffcc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ffcc-106">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7ffcc-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffcc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ffcc-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="7ffcc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ffcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ffcc-109">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="7ffcc-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="7ffcc-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7ffcc-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7ffcc-111">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="7ffcc-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="7ffcc-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7ffcc-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ffcc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ffcc-113">Return value</span></span>

<span data-ttu-id="7ffcc-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7ffcc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ffcc-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ffcc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ffcc-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="7ffcc-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ffcc-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7ffcc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ffcc-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ffcc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ffcc-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7ffcc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ffcc-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7ffcc-120">Requirements</span></span>



| <span data-ttu-id="7ffcc-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7ffcc-121">Requirement</span></span> | <span data-ttu-id="7ffcc-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7ffcc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffcc-123">Header</span><span class="sxs-lookup"><span data-stu-id="7ffcc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7ffcc-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ffcc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ffcc-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ffcc-125">Library</span></span><br/> | <dl> <span data-ttu-id="7ffcc-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ffcc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ffcc-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7ffcc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffcc-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="7ffcc-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




