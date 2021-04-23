---
description: 'Метод Сетдефаултеффектб задает результат по умолчанию. Этот метод эквивалентен Иамтимелине:: Сетдефаултеффект, но принимает значение BSTR, а не указатель на GUID.'
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'Метод Иамтимелине:: Сетдефаултеффектб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a8722a195078cb032285e4ea2ac449ad045d54f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651781"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a><span data-ttu-id="a50f9-104">Метод Иамтимелине:: Сетдефаултеффектб</span><span class="sxs-lookup"><span data-stu-id="a50f9-104">IAMTimeline::SetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="a50f9-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a50f9-105">\[Deprecated.</span></span> <span data-ttu-id="a50f9-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a50f9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a50f9-107">`SetDefaultEffectB`Метод задает результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a50f9-107">The `SetDefaultEffectB` method sets the default effect.</span></span> <span data-ttu-id="a50f9-108">Этот метод эквивалентен [**иамтимелине:: сетдефаултеффект**](iamtimeline-setdefaulteffect.md), но принимает значение BSTR, а не указатель на GUID.</span><span class="sxs-lookup"><span data-stu-id="a50f9-108">This method is equivalent to [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md), but takes a BSTR value, rather than a pointer to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="a50f9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a50f9-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="a50f9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a50f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50f9-111">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="a50f9-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="a50f9-112">Значение BSTR, представляющее идентификатор GUID для действия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a50f9-112">BSTR value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50f9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a50f9-113">Return value</span></span>

<span data-ttu-id="a50f9-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a50f9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a50f9-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a50f9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a50f9-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a50f9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a50f9-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a50f9-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a50f9-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a50f9-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a50f9-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a50f9-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a50f9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a50f9-120">Requirements</span></span>



| <span data-ttu-id="a50f9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a50f9-121">Requirement</span></span> | <span data-ttu-id="a50f9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a50f9-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a50f9-123">Header</span><span class="sxs-lookup"><span data-stu-id="a50f9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a50f9-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a50f9-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a50f9-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a50f9-125">Library</span></span><br/> | <dl> <span data-ttu-id="a50f9-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a50f9-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a50f9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a50f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a50f9-128">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="a50f9-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="a50f9-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a50f9-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




