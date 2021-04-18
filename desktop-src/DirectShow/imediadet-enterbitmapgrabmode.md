---
description: Метод Ентербитмапграбмоде переключает средство обнаружения мультимедиа в режим захвата точечного рисунка и выполняет поиск графа фильтра в указанное время.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Метод Имедиадет:: Ентербитмапграбмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675544"
---
# <a name="imediadetenterbitmapgrabmode-method"></a><span data-ttu-id="d2d22-103">Метод Имедиадет:: Ентербитмапграбмоде</span><span class="sxs-lookup"><span data-stu-id="d2d22-103">IMediaDet::EnterBitmapGrabMode method</span></span>

> [!Note]  
> <span data-ttu-id="d2d22-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d2d22-104">\[Deprecated.</span></span> <span data-ttu-id="d2d22-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2d22-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2d22-106">`EnterBitmapGrabMode`Метод переключает средство обнаружения мультимедиа в режим захвата точечного рисунка и выполняет поиск графа фильтра в указанное время.</span><span class="sxs-lookup"><span data-stu-id="d2d22-106">The `EnterBitmapGrabMode` method switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d22-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2d22-107">Syntax</span></span>


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a><span data-ttu-id="d2d22-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2d22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d22-109">*стреамтиме*</span><span class="sxs-lookup"><span data-stu-id="d2d22-109">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d22-110">Время в секундах, в течение которого граф ищет.</span><span class="sxs-lookup"><span data-stu-id="d2d22-110">Time, in seconds, to which the graph seeks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d22-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2d22-111">Return value</span></span>

<span data-ttu-id="d2d22-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2d22-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d2d22-113">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="d2d22-113">Possible values include the following:</span></span>



| <span data-ttu-id="d2d22-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d2d22-114">Return code</span></span>                                                                                             | <span data-ttu-id="d2d22-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d2d22-115">Description</span></span>                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="d2d22-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d22-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="d2d22-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d2d22-117">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d2d22-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d22-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="d2d22-119">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="d2d22-119">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="d2d22-120"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d22-120"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="d2d22-121">Исходный файл не содержит поток видео.</span><span class="sxs-lookup"><span data-stu-id="d2d22-121">The source file does not have a video stream.</span></span><br/> |
| <dl> <span data-ttu-id="d2d22-122"><dt>**присвоено \_ \_ время действия VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d22-122"><dt>**VFW\_E\_TIME\_EXPIRED**</dt></span></span> </dl>    | <span data-ttu-id="d2d22-123">Время ожидания команды поиска истекло.</span><span class="sxs-lookup"><span data-stu-id="d2d22-123">Seek command timed out.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="d2d22-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2d22-124">Remarks</span></span>

<span data-ttu-id="d2d22-125">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="d2d22-125">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="d2d22-126">Этот метод вставляет [**образец фильтра захвата**](sample-grabber-filter.md) в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="d2d22-126">This method inserts the [**Sample Grabber**](sample-grabber-filter.md) filter into the filter graph.</span></span> <span data-ttu-id="d2d22-127">Затем можно вызвать метод [**имедиадет:: жетсамплеграббер**](imediadet-getsamplegrabber.md) , чтобы получить указатель на интерфейс [**исамплеграббер**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="d2d22-127">You can then call [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) to obtain a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span> <span data-ttu-id="d2d22-128">Когда средство обнаружения мультимедиа переходит в режим захвата точечного рисунка, различные информационные методы в **имедиадет** не работают.</span><span class="sxs-lookup"><span data-stu-id="d2d22-128">Once the media detector enters bitmap grab mode, the various informational methods in **IMediaDet** do not work.</span></span>

<span data-ttu-id="d2d22-129">Методы [**имедиадет:: жетбитмапбитс**](imediadet-getbitmapbits.md) или [**Имедиадет:: вритебитмапбитс**](imediadet-writebitmapbits.md) также помещают детектор мультимедиа в режим захвата точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="d2d22-129">The [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) methods also put the media detector into bitmap grab mode.</span></span>

> [!Note]  
> <span data-ttu-id="d2d22-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d2d22-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2d22-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2d22-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d2d22-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d2d22-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2d22-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d2d22-133">Requirements</span></span>



| <span data-ttu-id="d2d22-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d2d22-134">Requirement</span></span> | <span data-ttu-id="d2d22-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d2d22-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d22-136">Header</span><span class="sxs-lookup"><span data-stu-id="d2d22-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d2d22-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d22-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d2d22-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2d22-138">Library</span></span><br/> | <dl> <span data-ttu-id="d2d22-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2d22-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d22-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2d22-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d22-141">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="d2d22-141">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="d2d22-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="d2d22-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




