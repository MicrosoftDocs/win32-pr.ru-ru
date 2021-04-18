---
description: Метод Сетмедиатипе указывает тип носителя для соединения во входном закрепления образца захвата.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'Метод Исамплеграббер:: Сетмедиатипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679863"
---
# <a name="isamplegrabbersetmediatype-method"></a><span data-ttu-id="3229f-103">Метод Исамплеграббер:: Сетмедиатипе</span><span class="sxs-lookup"><span data-stu-id="3229f-103">ISampleGrabber::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="3229f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3229f-104">\[Deprecated.</span></span> <span data-ttu-id="3229f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3229f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3229f-106">`SetMediaType`Метод задает тип носителя для соединения во входном закрепления образца захвата.</span><span class="sxs-lookup"><span data-stu-id="3229f-106">The `SetMediaType` method specifies the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="3229f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3229f-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="3229f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3229f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3229f-109">*птипе*</span><span class="sxs-lookup"><span data-stu-id="3229f-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="3229f-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) указывает требуемый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="3229f-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specifies the required media type.</span></span> <span data-ttu-id="3229f-111">Устанавливать все члены структуры необязательно; Дополнительные сведения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="3229f-111">It is not necessary to set all the structure members; see Remarks for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3229f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3229f-112">Return value</span></span>

<span data-ttu-id="3229f-113">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3229f-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3229f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3229f-114">Remarks</span></span>

<span data-ttu-id="3229f-115">По умолчанию образец захвата не имеет предпочтительного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="3229f-115">By default, the Sample Grabber has no preferred media type.</span></span> <span data-ttu-id="3229f-116">Чтобы обеспечить подключение образца захвата к правильному фильтру, вызовите этот метод перед построением графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="3229f-116">To ensure that the Sample Grabber connects to the correct filter, call this method before building the filter graph.</span></span>

<span data-ttu-id="3229f-117">Этот метод позволяет ограничивать диапазон типов мультимедиа, которые будет принимать фильтр.</span><span class="sxs-lookup"><span data-stu-id="3229f-117">This method restricts the range of media types that the filter will accept.</span></span> <span data-ttu-id="3229f-118">Когда фильтр подключается, он пытается сопоставить тип носителя, указанный в *птипе*.</span><span class="sxs-lookup"><span data-stu-id="3229f-118">When the filter connects, it tries to match the media type given in *pType*.</span></span> <span data-ttu-id="3229f-119">Для этого в этом порядке сравниваются основные GUID типа, подтип и тип формата.</span><span class="sxs-lookup"><span data-stu-id="3229f-119">To do so, it compares the major type, subtype, and format type GUIDs, in that order.</span></span> <span data-ttu-id="3229f-120">Для каждого из этих идентификаторов GUID, если *птипе* имеет значение GUID \_ null, образец захвата принимает тип мультимедиа без каких бы то ни было дополнительных проверок.</span><span class="sxs-lookup"><span data-stu-id="3229f-120">For each of these GUIDs, if *pType* has the value GUID\_NULL, the Sample Grabber accepts the media type without any further checks.</span></span> <span data-ttu-id="3229f-121">Если *птипе* имеет любое другое значение, то средство захвата выборки сравнивает его с идентификатором GUID в типе соединения.</span><span class="sxs-lookup"><span data-stu-id="3229f-121">If *pType* has any other value, the Sample Grabber compares it to the GUID in the connection type.</span></span> <span data-ttu-id="3229f-122">Если два идентификатора GUID точно не совпадают, то выборка отклоняет соединение.</span><span class="sxs-lookup"><span data-stu-id="3229f-122">Unless the two GUIDs match exactly, the Sample Grabber rejects the connection.</span></span>

<span data-ttu-id="3229f-123">Для видеороликов выборка блока форматирования пропускается.</span><span class="sxs-lookup"><span data-stu-id="3229f-123">For video media types, the Sample Grabber ignores the format block.</span></span> <span data-ttu-id="3229f-124">Таким образом, он будет принимать любой размер видео и частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="3229f-124">Therefore, it will accept any video size and frame rate.</span></span> <span data-ttu-id="3229f-125">При вызове `SetMediaType` Задайте для блока формата (**Пбформат**) **значение NULL** и размер (**кбформат**) равным нулю.</span><span class="sxs-lookup"><span data-stu-id="3229f-125">When you call `SetMediaType`, set the format block (**pbFormat**) to **NULL** and the size (**cbFormat**) to zero.</span></span> <span data-ttu-id="3229f-126">Для типов звуковых носителей образец блока записи проверит структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) и потребует, чтобы другой фильтр подключаться к этому формату, если только блок формата в *Птипе* не имеет **значение NULL**, или тег format имеет \_ формат PCM, \_ а другие члены структуры равны нулю.</span><span class="sxs-lookup"><span data-stu-id="3229f-126">For audio media types, the Sample Grabber will examine the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure and will require the other filter to connect with that format — unless the format block in *pType* is **NULL**, or the format tag is WAVE\_FORMAT\_PCM and the other structure members are zero.</span></span>

<span data-ttu-id="3229f-127">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="3229f-127">Example 1:</span></span>

-   <span data-ttu-id="3229f-128">Основной тип: \_ видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="3229f-128">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="3229f-129">Подтип: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="3229f-129">Subtype: GUID\_NULL</span></span>
-   <span data-ttu-id="3229f-130">Тип формата: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="3229f-130">Format type: GUID\_NULL</span></span>

<span data-ttu-id="3229f-131">Образец захвата примет все типы видеороликов, в которых основной тип совпадает с \_ видео MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="3229f-131">The Sample Grabber will accept any video type where the major type equals MEDIATYPE\_Video.</span></span> <span data-ttu-id="3229f-132">Подтип не будет проверяться.</span><span class="sxs-lookup"><span data-stu-id="3229f-132">It will not check the subtype.</span></span>

<span data-ttu-id="3229f-133">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="3229f-133">Example 2:</span></span>

-   <span data-ttu-id="3229f-134">Основной тип: \_ видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="3229f-134">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="3229f-135">Подтип: МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="3229f-135">Subtype: MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="3229f-136">Тип формата: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="3229f-136">Format type: GUID\_NULL</span></span>

<span data-ttu-id="3229f-137">Теперь образец захвата будет проверять подтип и принимать только RGB 24 видео.</span><span class="sxs-lookup"><span data-stu-id="3229f-137">Now the Sample Grabber will check the subtype, and accept only RGB 24 video.</span></span>

<span data-ttu-id="3229f-138">**Ограничения.** Независимо от того, какой тип задается, фильтр захвата выборки отклоняет все типы видео с ориентацией сверху вниз (отрицательное *бихеигхт*) или с типом формата \_ VideoInfo2.</span><span class="sxs-lookup"><span data-stu-id="3229f-138">**Limitations:** Regardless of what type you set, the Sample Grabber Filter rejects any video types with top-down orientation (negative *biHeight*), or with a format type of FORMAT\_VideoInfo2.</span></span> <span data-ttu-id="3229f-139">В этом случае, хотя `SetMediaType` метод выполняется правильно, фильтр не будет подключаться.</span><span class="sxs-lookup"><span data-stu-id="3229f-139">In this case, although the `SetMediaType` method succeeds, the filter will not connect.</span></span>

> [!Note]  
> <span data-ttu-id="3229f-140">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="3229f-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3229f-141">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3229f-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3229f-142">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3229f-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3229f-143">Требования</span><span class="sxs-lookup"><span data-stu-id="3229f-143">Requirements</span></span>



| <span data-ttu-id="3229f-144">Требование</span><span class="sxs-lookup"><span data-stu-id="3229f-144">Requirement</span></span> | <span data-ttu-id="3229f-145">Значение</span><span class="sxs-lookup"><span data-stu-id="3229f-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3229f-146">Header</span><span class="sxs-lookup"><span data-stu-id="3229f-146">Header</span></span><br/>  | <dl> <span data-ttu-id="3229f-147"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="3229f-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3229f-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3229f-148">Library</span></span><br/> | <dl> <span data-ttu-id="3229f-149"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3229f-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3229f-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3229f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3229f-151">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="3229f-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="3229f-152">**Интерфейс Исамплеграббер**</span><span class="sxs-lookup"><span data-stu-id="3229f-152">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 
