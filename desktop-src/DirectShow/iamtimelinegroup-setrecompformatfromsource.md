---
description: Метод Сетрекомпформатфромсаурце задает формат повторного сжатия видео, используя формат сжатия из исходного файла.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Метод Иамтимелинеграуп:: Сетрекомпформатфромсаурце (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679734"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a><span data-ttu-id="90dbb-103">Метод Иамтимелинеграуп:: Сетрекомпформатфромсаурце</span><span class="sxs-lookup"><span data-stu-id="90dbb-103">IAMTimelineGroup::SetRecompFormatFromSource method</span></span>

> [!Note]  
> <span data-ttu-id="90dbb-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="90dbb-104">\[Deprecated.</span></span> <span data-ttu-id="90dbb-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="90dbb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="90dbb-106">`SetRecompFormatFromSource`Метод задает формат повторного сжатия видео, используя формат сжатия из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="90dbb-106">The `SetRecompFormatFromSource` method sets the video recompression format using the compression format from a source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="90dbb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90dbb-107">Syntax</span></span>


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="90dbb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90dbb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90dbb-109">*псаурце*</span><span class="sxs-lookup"><span data-stu-id="90dbb-109">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="90dbb-110">Указатель на интерфейс [**иамтимелинесрк**](iamtimelinesrc.md) исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="90dbb-110">Pointer to the [**IAMTimelineSrc**](iamtimelinesrc.md) interface of the source object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90dbb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90dbb-111">Return value</span></span>

<span data-ttu-id="90dbb-112">Возвращает значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90dbb-112">Returns an **HRESULT** values.</span></span> <span data-ttu-id="90dbb-113">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="90dbb-113">Possible values include the following.</span></span>



| <span data-ttu-id="90dbb-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="90dbb-114">Return code</span></span>                                                                                             | <span data-ttu-id="90dbb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="90dbb-115">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90dbb-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="90dbb-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="90dbb-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="90dbb-117">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="90dbb-118"><dt>**\_нет \_ временной шкалы**</dt></span><span class="sxs-lookup"><span data-stu-id="90dbb-118"><dt>**E\_NO\_TIMELINE**</dt></span></span> </dl>          | <span data-ttu-id="90dbb-119">Группа находится за пределами временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="90dbb-119">The group is not within a timeline.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="90dbb-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="90dbb-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="90dbb-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="90dbb-121">Insufficient memory.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="90dbb-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="90dbb-122"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="90dbb-123">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="90dbb-123">**NULL** pointer argument.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="90dbb-124"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="90dbb-124"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="90dbb-125">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="90dbb-125">Invalid media type.</span></span> <span data-ttu-id="90dbb-126">Группа не является видеогруппой, или исходный файл не имеет потока видео.</span><span class="sxs-lookup"><span data-stu-id="90dbb-126">The group is not a video group, or the source file has no video stream.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90dbb-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90dbb-127">Remarks</span></span>

<span data-ttu-id="90dbb-128">Этот метод находит исходный файл, связанный с *псаурце*, Извлекает тип носителя первого видеопотока в файле и задает формат сжатия группы с помощью этого типа.</span><span class="sxs-lookup"><span data-stu-id="90dbb-128">This method finds the source file associated with *pSource*, retrieves the media type of the first video stream in the file, and sets the group compression format using that type.</span></span> <span data-ttu-id="90dbb-129">Дополнительные сведения о форматах сжатия см. в разделе [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md).</span><span class="sxs-lookup"><span data-stu-id="90dbb-129">For more information about compression formats, see [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span></span>

> [!Note]  
> <span data-ttu-id="90dbb-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="90dbb-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="90dbb-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="90dbb-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="90dbb-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="90dbb-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90dbb-133">Требования</span><span class="sxs-lookup"><span data-stu-id="90dbb-133">Requirements</span></span>



| <span data-ttu-id="90dbb-134">Требование</span><span class="sxs-lookup"><span data-stu-id="90dbb-134">Requirement</span></span> | <span data-ttu-id="90dbb-135">Значение</span><span class="sxs-lookup"><span data-stu-id="90dbb-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90dbb-136">Header</span><span class="sxs-lookup"><span data-stu-id="90dbb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="90dbb-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="90dbb-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="90dbb-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="90dbb-138">Library</span></span><br/> | <dl> <span data-ttu-id="90dbb-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90dbb-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90dbb-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90dbb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90dbb-141">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="90dbb-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="90dbb-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="90dbb-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




