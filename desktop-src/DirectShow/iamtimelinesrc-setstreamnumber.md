---
description: Метод Сетстреамнумбер указывает, какой поток следует считать из исходного файла, связанного с этим исходным объектом.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Метод Иамтимелинесрк:: Сетстреамнумбер (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689034"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a><span data-ttu-id="558c3-103">Метод Иамтимелинесрк:: Сетстреамнумбер</span><span class="sxs-lookup"><span data-stu-id="558c3-103">IAMTimelineSrc::SetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="558c3-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="558c3-104">\[Deprecated.</span></span> <span data-ttu-id="558c3-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="558c3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="558c3-106">`SetStreamNumber`Метод указывает, какой поток следует считать из исходного файла, связанного с этим исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="558c3-106">The `SetStreamNumber` method specifies which stream to read from the source file associated with this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="558c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="558c3-107">Syntax</span></span>


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a><span data-ttu-id="558c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="558c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="558c3-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="558c3-109">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="558c3-110">Номер потока из набора потоков, соответствующих типу носителя родительской группы.</span><span class="sxs-lookup"><span data-stu-id="558c3-110">The stream number, from the set of streams matching the media type of the parent group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="558c3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="558c3-111">Return value</span></span>

<span data-ttu-id="558c3-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="558c3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="558c3-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="558c3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="558c3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="558c3-114">Remarks</span></span>

<span data-ttu-id="558c3-115">Параметр *Val* указывает номер потока из набора потоков, который соответствует типу носителя родительской группы, а не ко всему набору потоков в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="558c3-115">The *Val* parameter specifies a stream number from the set of streams that matches the parent group's media type, not from the entire set of streams in the source file.</span></span> <span data-ttu-id="558c3-116">Например, предположим, что файл содержит два потока видео и два звуковых потока.</span><span class="sxs-lookup"><span data-stu-id="558c3-116">For example, For example, suppose that a file contains two video streams and two audio streams.</span></span> <span data-ttu-id="558c3-117">Если исходный объект находится внутри видеогруппы, для параметра *Val* значение 0 выбирается первый поток видео.</span><span class="sxs-lookup"><span data-stu-id="558c3-117">If the source object is inside a video group, setting *Val* to 0 selects the first video stream.</span></span> <span data-ttu-id="558c3-118">Вызывающий объект отвечает за указание допустимого номера потока.</span><span class="sxs-lookup"><span data-stu-id="558c3-118">The caller is responsible for specifying a valid stream number.</span></span>

<span data-ttu-id="558c3-119">Номер потока по умолчанию равен нулю.</span><span class="sxs-lookup"><span data-stu-id="558c3-119">The stream number defaults to zero.</span></span>

> [!Note]  
> <span data-ttu-id="558c3-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="558c3-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="558c3-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="558c3-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="558c3-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="558c3-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="558c3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="558c3-123">Requirements</span></span>



| <span data-ttu-id="558c3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="558c3-124">Requirement</span></span> | <span data-ttu-id="558c3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="558c3-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="558c3-126">Header</span><span class="sxs-lookup"><span data-stu-id="558c3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="558c3-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="558c3-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="558c3-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="558c3-128">Library</span></span><br/> | <dl> <span data-ttu-id="558c3-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="558c3-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="558c3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="558c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="558c3-131">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="558c3-131">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="558c3-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="558c3-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




