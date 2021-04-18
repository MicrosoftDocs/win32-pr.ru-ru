---
description: Метод Вритебитмапбитс извлекает кадр видео в указанное время мультимедиа и записывает его в файл. Кадр видео всегда находится в 24-разрядном формате RGB.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'Метод Имедиадет:: Вритебитмапбитс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675437"
---
# <a name="imediadetwritebitmapbits-method"></a><span data-ttu-id="52402-104">Метод Имедиадет:: Вритебитмапбитс</span><span class="sxs-lookup"><span data-stu-id="52402-104">IMediaDet::WriteBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="52402-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="52402-105">\[Deprecated.</span></span> <span data-ttu-id="52402-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52402-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52402-107">`WriteBitmapBits`Метод извлекает кадр видео в указанное время мультимедиа и записывает его в файл.</span><span class="sxs-lookup"><span data-stu-id="52402-107">The `WriteBitmapBits` method retrieves a video frame at the specified media time and writes it to a file.</span></span> <span data-ttu-id="52402-108">Кадр видео всегда находится в 24-разрядном формате RGB.</span><span class="sxs-lookup"><span data-stu-id="52402-108">The video frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="52402-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52402-109">Syntax</span></span>


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a><span data-ttu-id="52402-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="52402-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52402-111">*стреамтиме*</span><span class="sxs-lookup"><span data-stu-id="52402-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="52402-112">Время извлечения кадра видео.</span><span class="sxs-lookup"><span data-stu-id="52402-112">Time at which to retrieve the video frame.</span></span>

</dd> <dt>

<span data-ttu-id="52402-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="52402-113">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="52402-114">Ширина изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="52402-114">Width of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="52402-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="52402-115">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="52402-116">Высота изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="52402-116">Height of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="52402-117">*Имя файла*</span><span class="sxs-lookup"><span data-stu-id="52402-117">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="52402-118">Путь к файлу, в котором нужно сохранить точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="52402-118">Path of the file in which to save the bitmap.</span></span> <span data-ttu-id="52402-119">Если файл уже существует, этот метод перезаписывает его.</span><span class="sxs-lookup"><span data-stu-id="52402-119">If the file already exists, this method overwrites it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52402-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52402-120">Return value</span></span>

<span data-ttu-id="52402-121">Возвращает \_ ОК успешно.</span><span class="sxs-lookup"><span data-stu-id="52402-121">Returns S\_OK it successful.</span></span> <span data-ttu-id="52402-122">В противном случае возвращает значение **HRESULT** , указывающее причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="52402-122">Otherwise, returns an **HRESULT** value that indicates the cause of the error.</span></span> <span data-ttu-id="52402-123">Ниже перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="52402-123">Possible error codes include the following:</span></span>



| <span data-ttu-id="52402-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="52402-124">Return code</span></span>                                                                                             | <span data-ttu-id="52402-125">Описание</span><span class="sxs-lookup"><span data-stu-id="52402-125">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52402-126"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="52402-126"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="52402-127">Не удалось добавить [**образец фильтра захвата**](sample-grabber-filter.md) к диаграмме.</span><span class="sxs-lookup"><span data-stu-id="52402-127">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="52402-128"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="52402-128"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="52402-129">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="52402-129">Failure.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="52402-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="52402-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="52402-131">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="52402-131">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="52402-132"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="52402-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="52402-133">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="52402-133">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="52402-134"><dt>**STG \_ E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="52402-134"><dt>**STG\_E\_ACCESSDENIED**</dt></span></span> </dl>     | <span data-ttu-id="52402-135">Не удается перезаписать файл.</span><span class="sxs-lookup"><span data-stu-id="52402-135">Cannot overwrite file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="52402-136"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="52402-136"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="52402-137">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="52402-137">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="52402-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52402-138">Remarks</span></span>

<span data-ttu-id="52402-139">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="52402-139">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="52402-140">Этот метод помещает средство обнаружения мультимедиа в режим захвата точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="52402-140">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="52402-141">После вызова этого метода различные методы потоковой информации в **имедиадет** не работают, если не создать новый экземпляр детектора мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="52402-141">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="52402-142">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="52402-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="52402-143">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="52402-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="52402-144">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="52402-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52402-145">Требования</span><span class="sxs-lookup"><span data-stu-id="52402-145">Requirements</span></span>



| <span data-ttu-id="52402-146">Требование</span><span class="sxs-lookup"><span data-stu-id="52402-146">Requirement</span></span> | <span data-ttu-id="52402-147">Значение</span><span class="sxs-lookup"><span data-stu-id="52402-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52402-148">Header</span><span class="sxs-lookup"><span data-stu-id="52402-148">Header</span></span><br/>  | <dl> <span data-ttu-id="52402-149"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="52402-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="52402-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52402-150">Library</span></span><br/> | <dl> <span data-ttu-id="52402-151"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52402-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52402-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52402-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52402-153">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="52402-153">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="52402-154">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="52402-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




