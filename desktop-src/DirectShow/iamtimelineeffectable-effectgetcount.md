---
description: Метод Еффектжеткаунт извлекает количество эффектов для этого объекта.
ms.assetid: 6cf3b5b1-f38f-4ee1-8567-3c55f4f89cbb
title: 'Метод Иамтимелиниффектабле:: Еффектжеткаунт (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 247af794c2336c80e251d1a970e1d90925d4c53c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689501"
---
# <a name="iamtimelineeffectableeffectgetcount-method"></a><span data-ttu-id="d860d-103">Метод Иамтимелиниффектабле:: Еффектжеткаунт</span><span class="sxs-lookup"><span data-stu-id="d860d-103">IAMTimelineEffectable::EffectGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="d860d-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d860d-104">\[Deprecated.</span></span> <span data-ttu-id="d860d-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d860d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d860d-106">`EffectGetCount`Метод получает количество эффектов для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d860d-106">The `EffectGetCount` method retrieves the number of effects on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d860d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d860d-107">Syntax</span></span>


```C++
HRESULT EffectGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="d860d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d860d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d860d-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="d860d-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="d860d-110">Получает количество эффектов.</span><span class="sxs-lookup"><span data-stu-id="d860d-110">Receives the number of effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d860d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d860d-111">Return value</span></span>

<span data-ttu-id="d860d-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d860d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d860d-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d860d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d860d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d860d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d860d-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d860d-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d860d-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d860d-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d860d-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d860d-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d860d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d860d-118">Requirements</span></span>



| <span data-ttu-id="d860d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d860d-119">Requirement</span></span> | <span data-ttu-id="d860d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d860d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d860d-121">Header</span><span class="sxs-lookup"><span data-stu-id="d860d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d860d-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d860d-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d860d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d860d-123">Library</span></span><br/> | <dl> <span data-ttu-id="d860d-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d860d-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d860d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d860d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d860d-126">**Интерфейс Иамтимелиниффектабле**</span><span class="sxs-lookup"><span data-stu-id="d860d-126">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="d860d-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d860d-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




