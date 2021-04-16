---
description: Метод Буфферкб — это метод обратного вызова, который получает указатель на образец буфера.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'Метод Исамплеграбберкб:: Буфферкб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679862"
---
# <a name="isamplegrabbercbbuffercb-method"></a><span data-ttu-id="52322-103">Метод Исамплеграбберкб:: Буфферкб</span><span class="sxs-lookup"><span data-stu-id="52322-103">ISampleGrabberCB::BufferCB method</span></span>

> [!Note]  
> <span data-ttu-id="52322-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="52322-104">\[Deprecated.</span></span> <span data-ttu-id="52322-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52322-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52322-106">Метод **буфферкб** — это метод обратного вызова, который получает указатель на образец буфера.</span><span class="sxs-lookup"><span data-stu-id="52322-106">The **BufferCB** method is a callback method that receives a pointer to the sample buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="52322-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52322-107">Syntax</span></span>


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a><span data-ttu-id="52322-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52322-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52322-109">*самплетиме*</span><span class="sxs-lookup"><span data-stu-id="52322-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="52322-110">Время начала выборки в секундах.</span><span class="sxs-lookup"><span data-stu-id="52322-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="52322-111">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="52322-111">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="52322-112">Указатель на буфер, содержащий образец данных.</span><span class="sxs-lookup"><span data-stu-id="52322-112">Pointer to a buffer that contains the sample data.</span></span> <span data-ttu-id="52322-113">Формат данных зависит от типа носителя входного ПИН-кода захвата выборки.</span><span class="sxs-lookup"><span data-stu-id="52322-113">The format of the data depends on the media type of the Sample Grabber's input pin.</span></span> <span data-ttu-id="52322-114">Чтобы получить тип мультимедиа, вызовите [**исамплеграббер:: жетконнектедмедиатипе**](isamplegrabber-getconnectedmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="52322-114">To get the media type, call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="52322-115">*буфферлен*</span><span class="sxs-lookup"><span data-stu-id="52322-115">*BufferLen*</span></span> 
</dt> <dd>

<span data-ttu-id="52322-116">Длина буфера, на который указывает *pBuffer*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="52322-116">Length of the buffer pointed to by *pBuffer*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52322-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52322-117">Return value</span></span>

<span data-ttu-id="52322-118">Возвращает значение \_ ОК в случае успеха или код ошибки **HRESULT** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="52322-118">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="52322-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52322-119">Remarks</span></span>

<span data-ttu-id="52322-120">Этот метод обратного вызова получает указатель на данные в последнем примере носителя.</span><span class="sxs-lookup"><span data-stu-id="52322-120">This callback method receives a pointer to the data in the most recent media sample.</span></span>

> [!Note]  
> <span data-ttu-id="52322-121">Этот метод получает указатель на исходный образец данных, а не копию.</span><span class="sxs-lookup"><span data-stu-id="52322-121">This method receives a pointer to the original sample data, not a copy.</span></span> <span data-ttu-id="52322-122">Исходная документация неправильно объявила, что *pBuffer* содержит копию данных.</span><span class="sxs-lookup"><span data-stu-id="52322-122">The original documentation incorrectly stated that *pBuffer* contains a copy of the data.</span></span>

 

<span data-ttu-id="52322-123">Чтобы настроить обратный вызов, вызовите [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="52322-123">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="52322-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="52322-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="52322-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="52322-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="52322-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="52322-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52322-127">Требования</span><span class="sxs-lookup"><span data-stu-id="52322-127">Requirements</span></span>



| <span data-ttu-id="52322-128">Требование</span><span class="sxs-lookup"><span data-stu-id="52322-128">Requirement</span></span> | <span data-ttu-id="52322-129">Значение</span><span class="sxs-lookup"><span data-stu-id="52322-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52322-130">Header</span><span class="sxs-lookup"><span data-stu-id="52322-130">Header</span></span><br/>  | <dl> <span data-ttu-id="52322-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="52322-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="52322-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52322-132">Library</span></span><br/> | <dl> <span data-ttu-id="52322-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52322-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52322-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52322-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52322-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="52322-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="52322-136">**Интерфейс Исамплеграбберкб**</span><span class="sxs-lookup"><span data-stu-id="52322-136">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




