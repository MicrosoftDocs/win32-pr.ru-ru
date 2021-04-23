---
description: Метод Енаблиффектс включает или отключает все эффекты на временной шкале. Если эффекты отключены, они остаются на временной шкале, но не подготавливаются к просмотру.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'Метод Иамтимелине:: Енаблиффектс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675290"
---
# <a name="iamtimelineenableeffects-method"></a><span data-ttu-id="4a872-104">Метод Иамтимелине:: Енаблиффектс</span><span class="sxs-lookup"><span data-stu-id="4a872-104">IAMTimeline::EnableEffects method</span></span>

> [!Note]  
> <span data-ttu-id="4a872-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4a872-105">\[Deprecated.</span></span> <span data-ttu-id="4a872-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a872-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a872-107">`EnableEffects`Метод включает или отключает все эффекты на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="4a872-107">The `EnableEffects` method enables or disables all effects in the timeline.</span></span> <span data-ttu-id="4a872-108">Если эффекты отключены, они остаются на временной шкале, но не подготавливаются к просмотру.</span><span class="sxs-lookup"><span data-stu-id="4a872-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a872-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a872-109">Syntax</span></span>


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="4a872-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a872-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a872-111">*фенаблед*</span><span class="sxs-lookup"><span data-stu-id="4a872-111">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="4a872-112">Логическое значение, указывающее, следует ли включать или отключать эффекты.</span><span class="sxs-lookup"><span data-stu-id="4a872-112">Boolean value that specifies whether to enable or disable effects.</span></span> <span data-ttu-id="4a872-113">Если **значение равно true**, эффекты включены.</span><span class="sxs-lookup"><span data-stu-id="4a872-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="4a872-114">Если задано **значение false**, эффекты отключены.</span><span class="sxs-lookup"><span data-stu-id="4a872-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a872-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a872-115">Return value</span></span>

<span data-ttu-id="4a872-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4a872-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a872-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a872-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a872-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a872-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a872-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4a872-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a872-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a872-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a872-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4a872-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a872-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4a872-122">Requirements</span></span>



| <span data-ttu-id="4a872-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4a872-123">Requirement</span></span> | <span data-ttu-id="4a872-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4a872-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a872-125">Header</span><span class="sxs-lookup"><span data-stu-id="4a872-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4a872-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a872-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a872-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a872-127">Library</span></span><br/> | <dl> <span data-ttu-id="4a872-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a872-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a872-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a872-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a872-130">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="4a872-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="4a872-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="4a872-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




