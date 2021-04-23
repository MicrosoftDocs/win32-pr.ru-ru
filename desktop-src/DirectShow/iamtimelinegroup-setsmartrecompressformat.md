---
description: Метод Сетсмартрекомпрессформат задает формат сжатия видео, используемый для интеллектуального повторного сжатия.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'Метод Иамтимелинеграуп:: Сетсмартрекомпрессформат (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689210"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a><span data-ttu-id="3ed74-103">Метод Иамтимелинеграуп:: Сетсмартрекомпрессформат</span><span class="sxs-lookup"><span data-stu-id="3ed74-103">IAMTimelineGroup::SetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="3ed74-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3ed74-104">\[Deprecated.</span></span> <span data-ttu-id="3ed74-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3ed74-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3ed74-106">`SetSmartRecompressFormat`Метод задает формат сжатия видео, используемый для интеллектуального повторного сжатия.</span><span class="sxs-lookup"><span data-stu-id="3ed74-106">The `SetSmartRecompressFormat` method specifies a video compression format to use for smart recompression.</span></span>

<span data-ttu-id="3ed74-107">Смарт-сжатие не поддерживается для звуковых групп.</span><span class="sxs-lookup"><span data-stu-id="3ed74-107">Smart recompression is not supported for audio groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed74-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ed74-108">Syntax</span></span>


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3ed74-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ed74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed74-110">*пформат*</span><span class="sxs-lookup"><span data-stu-id="3ed74-110">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed74-111">Указатель на структуру, описывающую формат сжатия.</span><span class="sxs-lookup"><span data-stu-id="3ed74-111">Pointer to a structure describing the compression format.</span></span> <span data-ttu-id="3ed74-112">В настоящее время допустима только структура [**SCompFmt0**](scompfmt0.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed74-112">Currently, only the [**SCompFmt0**](scompfmt0.md) structure is valid.</span></span> <span data-ttu-id="3ed74-113">Этот параметр необходимо привести к указателю типа **Long**.</span><span class="sxs-lookup"><span data-stu-id="3ed74-113">You must cast this parameter to a pointer of type **long**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed74-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ed74-114">Return value</span></span>

<span data-ttu-id="3ed74-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3ed74-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ed74-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ed74-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed74-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ed74-117">Remarks</span></span>

<span data-ttu-id="3ed74-118">Перед вызовом этого метода вызовите метод [**иамтимелинеграуп:: сетмедиатипе**](iamtimelinegroup-setmediatype.md) для той же группы, чтобы указать несжатый формат.</span><span class="sxs-lookup"><span data-stu-id="3ed74-118">Before calling this method, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method on the same group, to specify an uncompressed format.</span></span>

<span data-ttu-id="3ed74-119">Если `SetSmartRecompressFormat` метод выполняется, можно использовать интеллектуальный механизм визуализации для вывода потока сжатого видео.</span><span class="sxs-lookup"><span data-stu-id="3ed74-119">If the `SetSmartRecompressFormat` method succeeds, you can use the Smart Render Engine to output a compressed video stream.</span></span> <span data-ttu-id="3ed74-120">Размер сжатого видео будет задаваться по ширине, высоте и частоте кадров, указанным в параметре *пформат* .</span><span class="sxs-lookup"><span data-stu-id="3ed74-120">The compressed video will have the width, height, and frame rate that was specified in the *pFormat* parameter.</span></span> <span data-ttu-id="3ed74-121">Эти значения будут переопределять параметры, заданные для формата несжатых данных в методе **сетмедиатипе** .</span><span class="sxs-lookup"><span data-stu-id="3ed74-121">These values will override those given for the uncompressed format in the **SetMediaType** method.</span></span> <span data-ttu-id="3ed74-122">Однако для получения преимуществ интеллектуального повторного сжатия два формата должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="3ed74-122">However, to get the benefits of smart recompression, the two formats should match.</span></span> <span data-ttu-id="3ed74-123">Иными словами, сжатые и несжатые форматы должны иметь одинаковую высоту, ширину и частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="3ed74-123">In other words, the compressed and uncompressed formats should have the same height, width, and frame rate.</span></span>

<span data-ttu-id="3ed74-124">Если модулю интеллектуального просмотра не удается создать сжатый формат, вместо него создается несжатый поток видео.</span><span class="sxs-lookup"><span data-stu-id="3ed74-124">If the Smart Render Engine is unable to produce the compressed format, it will produce an uncompressed video stream instead.</span></span> <span data-ttu-id="3ed74-125">Если это происходит, модуль интеллектуального просмотра отчетов сообщает \_ идентификаторы DEX не \_ удается \_ найти \_ ошибку отрисовки программы сжатия во время метода [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed74-125">If that occurs, the Smart Render Engine reports a DEX\_IDS\_CANT\_FIND\_COMPRESSOR rendering error during the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="3ed74-126">Приложение может перехватить эту ошибку с помощью метода [**иамеррорлог:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed74-126">The application can catch this error through the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="3ed74-127">(Дополнительные сведения см. в разделе [ведение журнала ошибок](logging-errors.md) и [отрисовка ошибок](rendering-errors.md).)</span><span class="sxs-lookup"><span data-stu-id="3ed74-127">(For more information, see [Logging Errors](logging-errors.md) and [Rendering Errors](rendering-errors.md).)</span></span>

<span data-ttu-id="3ed74-128">Формат смарт-сжатия не является постоянным.</span><span class="sxs-lookup"><span data-stu-id="3ed74-128">The smart recompression format is not persistent.</span></span> <span data-ttu-id="3ed74-129">Если приложение использует интеллектуальное повторное сжатие, оно должно задавать формат повторного сжатия при загрузке файла проекта.</span><span class="sxs-lookup"><span data-stu-id="3ed74-129">If an application uses smart recompression, it must set the recompression format whenever it loads a project file.</span></span>

> [!Note]  
> <span data-ttu-id="3ed74-130">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="3ed74-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3ed74-131">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ed74-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3ed74-132">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3ed74-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ed74-133">Требования</span><span class="sxs-lookup"><span data-stu-id="3ed74-133">Requirements</span></span>



| <span data-ttu-id="3ed74-134">Требование</span><span class="sxs-lookup"><span data-stu-id="3ed74-134">Requirement</span></span> | <span data-ttu-id="3ed74-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3ed74-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed74-136">Header</span><span class="sxs-lookup"><span data-stu-id="3ed74-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3ed74-137"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed74-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3ed74-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3ed74-138">Library</span></span><br/> | <dl> <span data-ttu-id="3ed74-139"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ed74-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ed74-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ed74-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed74-141">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="3ed74-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="3ed74-142">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="3ed74-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="3ed74-143">Модуль интеллектуального просмотра</span><span class="sxs-lookup"><span data-stu-id="3ed74-143">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> <dt>

[<span data-ttu-id="3ed74-144">Запись проекта в файл</span><span class="sxs-lookup"><span data-stu-id="3ed74-144">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




