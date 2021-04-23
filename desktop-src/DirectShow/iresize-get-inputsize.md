---
description: Метод Get \_ инпутсизе возвращает текущий размер входных данных фильтра изменения.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Метод Иресизе:: get_InputSize (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679839"
---
# <a name="iresizeget_inputsize-method"></a><span data-ttu-id="601b5-103">Метод Иресизе:: Get \_ инпутсизе</span><span class="sxs-lookup"><span data-stu-id="601b5-103">IResize::get\_InputSize method</span></span>

> [!Note]  
> <span data-ttu-id="601b5-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="601b5-104">\[Deprecated.</span></span> <span data-ttu-id="601b5-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="601b5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="601b5-106">`get_InputSize`Метод возвращает текущий размер входных данных фильтра изменения.</span><span class="sxs-lookup"><span data-stu-id="601b5-106">The `get_InputSize` method returns the resizer filter's current input size.</span></span>

## <a name="syntax"></a><span data-ttu-id="601b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="601b5-107">Syntax</span></span>


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a><span data-ttu-id="601b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="601b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601b5-109">*пихеигхт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="601b5-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="601b5-110">Получает высоту видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="601b5-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="601b5-111">*пивидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="601b5-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="601b5-112">Получает ширину видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="601b5-112">Receives the video width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601b5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="601b5-113">Return value</span></span>

<span data-ttu-id="601b5-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="601b5-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="601b5-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="601b5-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="601b5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="601b5-116">Remarks</span></span>

<span data-ttu-id="601b5-117">Если входной ПИН-код фильтра не подключен, возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="601b5-117">If the filter's input pin is not connected, return an error code.</span></span> <span data-ttu-id="601b5-118">В противном случае верните ширину и высоту видео в соответствии с типом носителя входного контакта.</span><span class="sxs-lookup"><span data-stu-id="601b5-118">Otherwise, return the width and height of the video, as specified by the input pin's media type.</span></span>

> [!Note]  
> <span data-ttu-id="601b5-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="601b5-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="601b5-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="601b5-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="601b5-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="601b5-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="601b5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="601b5-122">Requirements</span></span>



| <span data-ttu-id="601b5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="601b5-123">Requirement</span></span> | <span data-ttu-id="601b5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="601b5-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="601b5-125">Версия</span><span class="sxs-lookup"><span data-stu-id="601b5-125">Version</span></span><br/> | <span data-ttu-id="601b5-126">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="601b5-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="601b5-127">Header</span><span class="sxs-lookup"><span data-stu-id="601b5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="601b5-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="601b5-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="601b5-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="601b5-129">Library</span></span><br/> | <dl> <span data-ttu-id="601b5-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="601b5-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="601b5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="601b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601b5-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="601b5-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="601b5-133">**Интерфейс Иресизе**</span><span class="sxs-lookup"><span data-stu-id="601b5-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




