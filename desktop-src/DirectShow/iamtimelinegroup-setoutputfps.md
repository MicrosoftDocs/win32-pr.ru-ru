---
description: Метод Сетаутпутфпс задает несжатую частоту выходного кадра для этой группы.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Метод Иамтимелинеграуп:: Сетаутпутфпс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689212"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a><span data-ttu-id="ec5e1-103">Метод Иамтимелинеграуп:: Сетаутпутфпс</span><span class="sxs-lookup"><span data-stu-id="ec5e1-103">IAMTimelineGroup::SetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="ec5e1-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-104">\[Deprecated.</span></span> <span data-ttu-id="ec5e1-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ec5e1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ec5e1-106">`SetOutputFPS`Метод задает несжатую частоту выходного кадра для этой группы.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-106">The `SetOutputFPS` method sets the uncompressed output frame rate for this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5e1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec5e1-107">Syntax</span></span>


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="ec5e1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec5e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5e1-109">*Кадры в секунду*</span><span class="sxs-lookup"><span data-stu-id="ec5e1-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5e1-110">Частота вывода кадров для этой группы, в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-110">Output frame rate for this group, in frames per second.</span></span> <span data-ttu-id="ec5e1-111">Значение не может равняться нулю и не может содержать более семи цифр после десятичного знака.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-111">The value cannot equal zero, and cannot have more than seven digits after the decimal place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5e1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec5e1-112">Return value</span></span>

<span data-ttu-id="ec5e1-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ec5e1-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec5e1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec5e1-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec5e1-115">Remarks</span></span>

<span data-ttu-id="ec5e1-116">Отображаемые выходные данные этой группы выполняются с заданной частотой кадров, и все изменения в исходном материале округляются до ближайшей границы фрейма, как определено частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-116">Rendered output from this group runs at the specified frame rate, and all edits on the source material are rounded to the nearest frame boundary, as defined by the frame rate.</span></span> <span data-ttu-id="ec5e1-117">Для лучшей производительности используйте одинаковую частоту кадров для всех групп, видео и аудио.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-117">For best performance, use the same frame rate for all groups, video and audio.</span></span>

<span data-ttu-id="ec5e1-118">Метод [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md) перезаписывает частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-118">The [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method overwrites the frame rate.</span></span>

> [!Note]  
> <span data-ttu-id="ec5e1-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ec5e1-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec5e1-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ec5e1-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ec5e1-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ec5e1-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec5e1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ec5e1-122">Requirements</span></span>



| <span data-ttu-id="ec5e1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ec5e1-123">Requirement</span></span> | <span data-ttu-id="ec5e1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ec5e1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5e1-125">Header</span><span class="sxs-lookup"><span data-stu-id="ec5e1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ec5e1-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec5e1-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ec5e1-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ec5e1-127">Library</span></span><br/> | <dl> <span data-ttu-id="ec5e1-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec5e1-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5e1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec5e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5e1-130">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="ec5e1-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="ec5e1-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ec5e1-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




