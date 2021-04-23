---
description: Метод Самплекб — это метод обратного вызова, который получает указатель на пример носителя.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'Метод Исамплеграбберкб:: Самплекб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679777"
---
# <a name="isamplegrabbercbsamplecb-method"></a><span data-ttu-id="e5c9e-103">Метод Исамплеграбберкб:: Самплекб</span><span class="sxs-lookup"><span data-stu-id="e5c9e-103">ISampleGrabberCB::SampleCB method</span></span>

> [!Note]  
> <span data-ttu-id="e5c9e-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e5c9e-104">\[Deprecated.</span></span> <span data-ttu-id="e5c9e-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e5c9e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e5c9e-106">`SampleCB`Метод является методом обратного вызова, который получает указатель на пример носителя.</span><span class="sxs-lookup"><span data-stu-id="e5c9e-106">The `SampleCB` method is a callback method that receives a pointer to the media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c9e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5c9e-107">Syntax</span></span>


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e5c9e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5c9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c9e-109">*самплетиме*</span><span class="sxs-lookup"><span data-stu-id="e5c9e-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c9e-110">Время начала выборки в секундах.</span><span class="sxs-lookup"><span data-stu-id="e5c9e-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="e5c9e-111">*псампле*</span><span class="sxs-lookup"><span data-stu-id="e5c9e-111">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c9e-112">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="e5c9e-112">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c9e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5c9e-113">Return value</span></span>

<span data-ttu-id="e5c9e-114">Возвращает значение \_ ОК в случае успеха или код ошибки **HRESULT** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e5c9e-114">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c9e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5c9e-115">Remarks</span></span>

<span data-ttu-id="e5c9e-116">Чтобы настроить обратный вызов, вызовите [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="e5c9e-116">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="e5c9e-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="e5c9e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e5c9e-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e5c9e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e5c9e-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e5c9e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5c9e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e5c9e-120">Requirements</span></span>



| <span data-ttu-id="e5c9e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e5c9e-121">Requirement</span></span> | <span data-ttu-id="e5c9e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e5c9e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c9e-123">Header</span><span class="sxs-lookup"><span data-stu-id="e5c9e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e5c9e-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c9e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e5c9e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5c9e-125">Library</span></span><br/> | <dl> <span data-ttu-id="e5c9e-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5c9e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c9e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5c9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c9e-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="e5c9e-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="e5c9e-129">**Интерфейс Исамплеграбберкб**</span><span class="sxs-lookup"><span data-stu-id="e5c9e-129">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




