---
description: 'Не поддерживается. Вызовите метод Иамтимелине:: Креатимптиноде, чтобы создать новый объект временной шкалы. После создания объекта изменить его тип нельзя.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'Метод Иамтимелинеобж:: Сеттимелинетипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689138"
---
# <a name="iamtimelineobjsettimelinetype-method"></a><span data-ttu-id="bd710-105">Метод Иамтимелинеобж:: Сеттимелинетипе</span><span class="sxs-lookup"><span data-stu-id="bd710-105">IAMTimelineObj::SetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="bd710-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bd710-106">\[Deprecated.</span></span> <span data-ttu-id="bd710-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bd710-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bd710-108">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bd710-108">Not supported.</span></span> <span data-ttu-id="bd710-109">Вызовите метод [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) , чтобы создать новый объект временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="bd710-109">Call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method to create a new timeline object.</span></span> <span data-ttu-id="bd710-110">После создания объекта изменить его тип нельзя.</span><span class="sxs-lookup"><span data-stu-id="bd710-110">Once an object is created, you cannot change its type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd710-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd710-111">Syntax</span></span>


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a><span data-ttu-id="bd710-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd710-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd710-113">*неввал*</span><span class="sxs-lookup"><span data-stu-id="bd710-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="bd710-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="bd710-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd710-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd710-115">Return value</span></span>

<span data-ttu-id="bd710-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd710-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd710-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd710-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd710-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd710-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bd710-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="bd710-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bd710-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd710-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bd710-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="bd710-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd710-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bd710-122">Requirements</span></span>



| <span data-ttu-id="bd710-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bd710-123">Requirement</span></span> | <span data-ttu-id="bd710-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bd710-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd710-125">Header</span><span class="sxs-lookup"><span data-stu-id="bd710-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bd710-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd710-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bd710-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bd710-127">Library</span></span><br/> | <dl> <span data-ttu-id="bd710-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd710-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd710-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd710-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd710-130">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="bd710-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




