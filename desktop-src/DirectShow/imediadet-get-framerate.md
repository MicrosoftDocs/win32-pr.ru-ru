---
description: Метод "получить \_ частоту кадров" получает скорость кадров текущего потока. Поток должен представлять собой поток видео.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Метод Имедиадет:: get_FrameRate (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679711"
---
# <a name="imediadetget_framerate-method"></a><span data-ttu-id="33375-104">Метод Имедиадет:: Get \_ частоты кадров</span><span class="sxs-lookup"><span data-stu-id="33375-104">IMediaDet::get\_FrameRate method</span></span>

> [!Note]  
> <span data-ttu-id="33375-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="33375-105">\[Deprecated.</span></span> <span data-ttu-id="33375-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="33375-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="33375-107">`get_FrameRate`Метод получает частоту кадров текущего потока.</span><span class="sxs-lookup"><span data-stu-id="33375-107">The `get_FrameRate` method retrieves the frame rate of the current stream.</span></span> <span data-ttu-id="33375-108">Поток должен представлять собой поток видео.</span><span class="sxs-lookup"><span data-stu-id="33375-108">The stream must be a video stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="33375-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33375-109">Syntax</span></span>


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="33375-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="33375-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33375-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="33375-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="33375-112">Получает частоту кадров в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="33375-112">Receives the frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33375-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33375-113">Return value</span></span>

<span data-ttu-id="33375-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33375-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="33375-115">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="33375-115">Possible values include the following:</span></span>



| <span data-ttu-id="33375-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="33375-116">Return code</span></span>                                                                                             | <span data-ttu-id="33375-117">Описание</span><span class="sxs-lookup"><span data-stu-id="33375-117">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="33375-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="33375-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="33375-119">В заголовке формата видео не указана частота кадров.</span><span class="sxs-lookup"><span data-stu-id="33375-119">Video format header does not specify a frame rate.</span></span><br/> |
| <dl> <span data-ttu-id="33375-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="33375-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="33375-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="33375-121">Success.</span></span><br/>                                           |
| <dl> <span data-ttu-id="33375-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="33375-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="33375-123">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="33375-123">Invalid argument.</span></span><br/>                                  |
| <dl> <span data-ttu-id="33375-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="33375-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="33375-125">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="33375-125">**NULL** pointer argument.</span></span><br/>                         |
| <dl> <span data-ttu-id="33375-126"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="33375-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="33375-127">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="33375-127">Invalid media type.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="33375-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33375-128">Remarks</span></span>

<span data-ttu-id="33375-129">Этот метод не может получить частоту кадров из ASF – файла.</span><span class="sxs-lookup"><span data-stu-id="33375-129">This method cannot retrieve the frame rate from an ASF file.</span></span>

<span data-ttu-id="33375-130">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="33375-130">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="33375-131">Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="33375-131">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="33375-132">Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="33375-132">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="33375-133">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="33375-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="33375-134">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="33375-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="33375-135">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="33375-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="33375-136">Требования</span><span class="sxs-lookup"><span data-stu-id="33375-136">Requirements</span></span>



| <span data-ttu-id="33375-137">Требование</span><span class="sxs-lookup"><span data-stu-id="33375-137">Requirement</span></span> | <span data-ttu-id="33375-138">Значение</span><span class="sxs-lookup"><span data-stu-id="33375-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33375-139">Header</span><span class="sxs-lookup"><span data-stu-id="33375-139">Header</span></span><br/>  | <dl> <span data-ttu-id="33375-140"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="33375-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="33375-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33375-141">Library</span></span><br/> | <dl> <span data-ttu-id="33375-142"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33375-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33375-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33375-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33375-144">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="33375-144">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="33375-145">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="33375-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




