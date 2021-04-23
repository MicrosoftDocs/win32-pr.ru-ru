---
description: Метод Сетаутпутбуфферинг задает число кадров, отображаемых заранее во время просмотра.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Метод Иамтимелинеграуп:: Сетаутпутбуфферинг (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689213"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a><span data-ttu-id="ccf94-103">Метод Иамтимелинеграуп:: Сетаутпутбуфферинг</span><span class="sxs-lookup"><span data-stu-id="ccf94-103">IAMTimelineGroup::SetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="ccf94-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ccf94-104">\[Deprecated.</span></span> <span data-ttu-id="ccf94-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ccf94-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ccf94-106">`SetOutputBuffering`Метод задает число кадров, отображаемых заранее во время просмотра.</span><span class="sxs-lookup"><span data-stu-id="ccf94-106">The `SetOutputBuffering` method specifies the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf94-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccf94-107">Syntax</span></span>


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ccf94-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccf94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf94-109">*нбуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ccf94-109">*nBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf94-110">Число кадров в буфере во время предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="ccf94-110">Number of frames to buffer during preview.</span></span> <span data-ttu-id="ccf94-111">Должно быть два или более.</span><span class="sxs-lookup"><span data-stu-id="ccf94-111">Must be two or greater.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf94-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccf94-112">Return value</span></span>

<span data-ttu-id="ccf94-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ccf94-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ccf94-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccf94-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf94-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccf94-115">Remarks</span></span>

<span data-ttu-id="ccf94-116">Буфер большего размера требует больше памяти, но может привести к более гладкому просмотру, особенно во время эффектов или переходов, требующих больше времени для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ccf94-116">A larger buffer requires more memory but can result in smoother previewing, especially during effects or transitions that require more time to render.</span></span> <span data-ttu-id="ccf94-117">Буфер по умолчанию — 30 кадров.</span><span class="sxs-lookup"><span data-stu-id="ccf94-117">The default buffer is 30 frames.</span></span>

> [!Note]  
> <span data-ttu-id="ccf94-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ccf94-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ccf94-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ccf94-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ccf94-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ccf94-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccf94-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ccf94-121">Requirements</span></span>



| <span data-ttu-id="ccf94-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ccf94-122">Requirement</span></span> | <span data-ttu-id="ccf94-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ccf94-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf94-124">Header</span><span class="sxs-lookup"><span data-stu-id="ccf94-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ccf94-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf94-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ccf94-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ccf94-126">Library</span></span><br/> | <dl> <span data-ttu-id="ccf94-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccf94-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf94-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccf94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf94-129">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="ccf94-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="ccf94-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ccf94-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




