---
description: 'Метод Жетдефаултфпс извлекает частоту кадров вывода по умолчанию в кадрах в секунду (кадров/с). Группы используют это значение в качестве частоты кадров по умолчанию. Чтобы задать частоту кадров группы, вызовите метод Иамтимелинеграуп:: Сетаутпутфпс в группе.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Метод Иамтимелине:: Жетдефаултфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675382"
---
# <a name="iamtimelinegetdefaultfps-method"></a><span data-ttu-id="700fe-105">Метод Иамтимелине:: Жетдефаултфпс</span><span class="sxs-lookup"><span data-stu-id="700fe-105">IAMTimeline::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="700fe-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="700fe-106">\[Deprecated.</span></span> <span data-ttu-id="700fe-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="700fe-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="700fe-108">`GetDefaultFPS`Метод извлекает частоту выходного кадра по умолчанию в кадрах в секунду (кадров/с).</span><span class="sxs-lookup"><span data-stu-id="700fe-108">The `GetDefaultFPS` method retrieves the default output frame rate, in frames per second (FPS).</span></span> <span data-ttu-id="700fe-109">Группы используют это значение в качестве частоты кадров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="700fe-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="700fe-110">Чтобы задать частоту кадров группы, вызовите метод [**иамтимелинеграуп:: сетаутпутфпс**](iamtimelinegroup-setoutputfps.md) в группе.</span><span class="sxs-lookup"><span data-stu-id="700fe-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="700fe-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="700fe-111">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="700fe-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="700fe-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="700fe-113">*пфпс*</span><span class="sxs-lookup"><span data-stu-id="700fe-113">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="700fe-114">Получает частоту кадров по умолчанию в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="700fe-114">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="700fe-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="700fe-115">Return value</span></span>

<span data-ttu-id="700fe-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="700fe-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="700fe-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="700fe-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="700fe-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="700fe-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="700fe-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="700fe-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="700fe-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="700fe-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="700fe-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="700fe-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="700fe-122">Требования</span><span class="sxs-lookup"><span data-stu-id="700fe-122">Requirements</span></span>



| <span data-ttu-id="700fe-123">Требование</span><span class="sxs-lookup"><span data-stu-id="700fe-123">Requirement</span></span> | <span data-ttu-id="700fe-124">Значение</span><span class="sxs-lookup"><span data-stu-id="700fe-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="700fe-125">Header</span><span class="sxs-lookup"><span data-stu-id="700fe-125">Header</span></span><br/>  | <dl> <span data-ttu-id="700fe-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="700fe-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="700fe-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="700fe-127">Library</span></span><br/> | <dl> <span data-ttu-id="700fe-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="700fe-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700fe-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="700fe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700fe-130">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="700fe-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="700fe-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="700fe-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




