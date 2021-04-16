---
description: 'Не поддерживается. Вместо этого вызовите метод Иамтимелине:: AddGroup.'
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'Метод Иамтимелинеграуп:: Сеттимелине (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679688"
---
# <a name="iamtimelinegroupsettimeline-method"></a><span data-ttu-id="c2cc3-104">Метод Иамтимелинеграуп:: Сеттимелине</span><span class="sxs-lookup"><span data-stu-id="c2cc3-104">IAMTimelineGroup::SetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="c2cc3-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-105">\[Deprecated.</span></span> <span data-ttu-id="c2cc3-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2cc3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c2cc3-107">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-107">Not supported.</span></span> <span data-ttu-id="c2cc3-108">Вместо этого вызовите метод [**иамтимелине:: addgroup**](iamtimeline-addgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="c2cc3-108">Call the [**IAMTimeline::AddGroup**](iamtimeline-addgroup.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cc3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2cc3-109">Syntax</span></span>


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="c2cc3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2cc3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cc3-111">*птимелине*</span><span class="sxs-lookup"><span data-stu-id="c2cc3-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cc3-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cc3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2cc3-113">Return value</span></span>

<span data-ttu-id="c2cc3-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2cc3-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2cc3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cc3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2cc3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2cc3-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c2cc3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c2cc3-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2cc3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c2cc3-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c2cc3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2cc3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c2cc3-120">Requirements</span></span>



| <span data-ttu-id="c2cc3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c2cc3-121">Requirement</span></span> | <span data-ttu-id="c2cc3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c2cc3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cc3-123">Header</span><span class="sxs-lookup"><span data-stu-id="c2cc3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c2cc3-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2cc3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c2cc3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2cc3-125">Library</span></span><br/> | <dl> <span data-ttu-id="c2cc3-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2cc3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cc3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2cc3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cc3-128">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="c2cc3-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




