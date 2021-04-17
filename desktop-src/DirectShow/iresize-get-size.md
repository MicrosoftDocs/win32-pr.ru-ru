---
description: Метод Get \_ Size возвращает текущий размер выходных данных и режим Stretch.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Метод Иресизе:: get_Size (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679837"
---
# <a name="iresizeget_size-method"></a><span data-ttu-id="2a7a0-103">Метод Иресизе:: Get \_ size</span><span class="sxs-lookup"><span data-stu-id="2a7a0-103">IResize::get\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="2a7a0-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-104">\[Deprecated.</span></span> <span data-ttu-id="2a7a0-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a7a0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2a7a0-106">`get_Size`Метод возвращает текущий размер выходных данных и режим Stretch.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-106">The `get_Size` method returns the current output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a7a0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a7a0-107">Syntax</span></span>


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a><span data-ttu-id="2a7a0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a7a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a7a0-109">*пихеигхт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a7a0-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7a0-110">Получает высоту видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2a7a0-111">*пивидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a7a0-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7a0-112">Получает ширину видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-112">Receives the video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2a7a0-113">*пфлаг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a7a0-113">*pFlag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7a0-114">Получает флаг, задающий режим растяжения.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-114">Receives a flag specifying the stretch mode.</span></span> <span data-ttu-id="2a7a0-115">Возможные значения см. в разделе [**изменение размера флагов**](resize-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="2a7a0-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a7a0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a7a0-116">Return value</span></span>

<span data-ttu-id="2a7a0-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2a7a0-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a7a0-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a7a0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a7a0-119">Remarks</span></span>

<span data-ttu-id="2a7a0-120">Если тип выходных данных не задан, фильтр должен вернуть значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-120">If the output type has not been set, the filter should return default values.</span></span> <span data-ttu-id="2a7a0-121">Эти значения можно произвольно выбрать во время разработки.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-121">These values can be arbitrarily chosen at design time.</span></span>

> [!Note]  
> <span data-ttu-id="2a7a0-122">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2a7a0-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2a7a0-123">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2a7a0-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2a7a0-124">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2a7a0-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a7a0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2a7a0-125">Requirements</span></span>



| <span data-ttu-id="2a7a0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2a7a0-126">Requirement</span></span> | <span data-ttu-id="2a7a0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2a7a0-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7a0-128">Версия</span><span class="sxs-lookup"><span data-stu-id="2a7a0-128">Version</span></span><br/> | <span data-ttu-id="2a7a0-129">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2a7a0-129">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="2a7a0-130">Header</span><span class="sxs-lookup"><span data-stu-id="2a7a0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2a7a0-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a7a0-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2a7a0-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a7a0-132">Library</span></span><br/> | <dl> <span data-ttu-id="2a7a0-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a7a0-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a7a0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a7a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7a0-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="2a7a0-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="2a7a0-136">**Интерфейс Иресизе**</span><span class="sxs-lookup"><span data-stu-id="2a7a0-136">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




