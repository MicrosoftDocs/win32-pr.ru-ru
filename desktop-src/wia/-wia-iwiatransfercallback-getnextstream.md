---
description: Возвращает новый поток для указанного элемента.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'Метод Ивиатрансферкаллбакк:: Жетнекстстреам (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692425"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a><span data-ttu-id="39e6a-103">Метод Ивиатрансферкаллбакк:: Жетнекстстреам</span><span class="sxs-lookup"><span data-stu-id="39e6a-103">IWiaTransferCallback::GetNextStream method</span></span>

<span data-ttu-id="39e6a-104">Возвращает новый поток для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="39e6a-104">Gets a new stream for the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e6a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39e6a-105">Syntax</span></span>


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a><span data-ttu-id="39e6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39e6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e6a-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39e6a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e6a-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="39e6a-108">Type: **LONG**</span></span>

<span data-ttu-id="39e6a-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="39e6a-109">Currently unused.</span></span> <span data-ttu-id="39e6a-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="39e6a-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="39e6a-111">*бстритемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39e6a-111">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e6a-112">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="39e6a-112">Type: **BSTR**</span></span>

<span data-ttu-id="39e6a-113">Указывает имя элемента, для которого создается поток.</span><span class="sxs-lookup"><span data-stu-id="39e6a-113">Specifies the name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="39e6a-114">*бстрфуллитемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39e6a-114">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e6a-115">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="39e6a-115">Type: **BSTR**</span></span>

<span data-ttu-id="39e6a-116">Указывает полное имя элемента, для которого создается поток.</span><span class="sxs-lookup"><span data-stu-id="39e6a-116">Specifies the full name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="39e6a-117">*ппдестинатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39e6a-117">*ppDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39e6a-118">Тип: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span><span class="sxs-lookup"><span data-stu-id="39e6a-118">Type: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span></span>

<span data-ttu-id="39e6a-119">Получает адрес указателя на новый объект [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="39e6a-119">Receives the address of a pointer to the new [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e6a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39e6a-120">Return value</span></span>

<span data-ttu-id="39e6a-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="39e6a-121">Type: **HRESULT**</span></span>

<span data-ttu-id="39e6a-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="39e6a-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39e6a-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39e6a-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e6a-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39e6a-124">Remarks</span></span>

<span data-ttu-id="39e6a-125">Если этот метод реализуется с помощью фильтра обработки изображений, то при получении образа Windows (WIA) 2,0 минидривер вызывает его во время получения изображения, чтобы получить целевой поток от клиента.</span><span class="sxs-lookup"><span data-stu-id="39e6a-125">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to get the destination stream from the client.</span></span>

<span data-ttu-id="39e6a-126">Фильтр **ивиатрансферкаллбакк:: жетнекстстреам** должен делегировать методу обратного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="39e6a-126">A filter's **IWiaTransferCallback::GetNextStream** must delegate to the application's callback method.</span></span> <span data-ttu-id="39e6a-127">Фильтр использует поток, возвращенный реализацией **ивиатрансферкаллбакк:: жетнекстстреам** обратного вызова приложения, чтобы создать собственный поток, который передается обратно в службу WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="39e6a-127">The filter uses the stream returned by the application callback's **IWiaTransferCallback::GetNextStream** implementation to create its own stream that it passes back to the WIA 2.0 service.</span></span> <span data-ttu-id="39e6a-128">Фильтрация выполняется, когда поток фильтра вызывает метод [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .</span><span class="sxs-lookup"><span data-stu-id="39e6a-128">The filtering is done when the filter's stream calls the [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method.</span></span>

<span data-ttu-id="39e6a-129">Поток фильтра не может делать никаких предположений о количестве байтов, записываемых в него при каждой записи, поскольку нефильтрованные данные изображения могут поступать из компонента предварительной версии WIA 2,0, а не драйвера.</span><span class="sxs-lookup"><span data-stu-id="39e6a-129">The filter's stream cannot make any assumptions on the number of bytes that are written to it on each write, since the unfiltered image data may come from the WIA 2.0 Preview Component rather than the driver.</span></span> <span data-ttu-id="39e6a-130">Компонент WIA 2,0 Preview всегда записывает все нефильтрованные данные изображения в поток фильтра только один раз, что означает, что поток фильтра имеет один источник.</span><span class="sxs-lookup"><span data-stu-id="39e6a-130">The WIA 2.0 Preview Component always writes the whole unfiltered image data into the filter's stream only once, which means that the filter's stream has one source writing into it.</span></span> <span data-ttu-id="39e6a-131">Если драйвер и компонент предварительного просмотра записывают данные в поток фильтра, поток фильтра не может предположить, например, что он получит полный заголовок при первом вызове [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , несмотря на то, что соответствующий драйвер всегда сначала записывает данных заголовка в одну запись.</span><span class="sxs-lookup"><span data-stu-id="39e6a-131">If both the driver and the preview component write into the filter's stream, the filter's stream cannot assume, for example, that it will receive the full header the first time [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) is called although its corresponding driver always writes the header data first in one write.</span></span> <span data-ttu-id="39e6a-132">Также нельзя предположить, что последующая запись содержит только одну строку сканирования.</span><span class="sxs-lookup"><span data-stu-id="39e6a-132">Nor can it assume that a subsequent write contains exactly one scan line.</span></span> <span data-ttu-id="39e6a-133">Поэтому потоку фильтрации может потребоваться подсчитать число байтов, записанных в него, чтобы определить, например, начало данных изображения.</span><span class="sxs-lookup"><span data-stu-id="39e6a-133">So the filtering stream may have to count the number of bytes written to it to determine, for example, where the image data starts.</span></span>

<span data-ttu-id="39e6a-134">Реализация **ивиатрансферкаллбакк:: жетнекстстреам** фильтра обработки изображений должна считывать свойства, необходимые для обработки изображения из элемента, для которого запрашивается изображение.</span><span class="sxs-lookup"><span data-stu-id="39e6a-134">The image processing filter's **IWiaTransferCallback::GetNextStream** implementation should read the properties needed for its image processing from the item for which the image is being acquired.</span></span> <span data-ttu-id="39e6a-135">Фильтр не считывает свойства непосредственно из *pWiaItem2* , переданного в [**инитиализефилтер**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="39e6a-135">The filter does not read the properties directly from the *pWiaItem2* passed into [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span> <span data-ttu-id="39e6a-136">Вместо этого фильтр должен вызвать [**финдитембинаме**](-wia-iwiaitem2-finditembyname.md) для этого элемента WIA 2,0, чтобы получить фактический элемент WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="39e6a-136">Instead the filter must call [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) on this WIA 2.0 item to obtain the actual WIA 2.0 item.</span></span> <span data-ttu-id="39e6a-137">Причина в том, что получаемый образ может фактически быть дочерним элементом *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="39e6a-137">The reason for this is that the image being acquired may actually be a child item of *pWiaItem2*.</span></span> <span data-ttu-id="39e6a-138">Например, во время приобретения папки фильтр использует *pWiaItem2* для получения дочерних элементов *pWiaItem2* в **ивиатрансферкаллбакк:: жетнекстстреам** (во время приобретения папки драйвер возвращает образы, представленные дочерними элементами *pWiaItem2*).</span><span class="sxs-lookup"><span data-stu-id="39e6a-138">For example, during a folder acquisition the filter uses *pWiaItem2* to obtain *pWiaItem2*'s child items in **IWiaTransferCallback::GetNextStream** (during a folder acquisition the driver returns the images represented by the child items of *pWiaItem2*).</span></span> <span data-ttu-id="39e6a-139">То же самое верно, когда компонент WIA 2,0 Preview вызывает фильтр обработки изображений, передающий дочерний элемент WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="39e6a-139">The same is true when the WIA 2.0 Preview Component calls into the image processing filter passing a child WIA 2.0 item.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e6a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="39e6a-140">Requirements</span></span>



| <span data-ttu-id="39e6a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="39e6a-141">Requirement</span></span> | <span data-ttu-id="39e6a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="39e6a-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e6a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39e6a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="39e6a-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39e6a-144">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="39e6a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39e6a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="39e6a-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39e6a-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="39e6a-147">Header</span><span class="sxs-lookup"><span data-stu-id="39e6a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="39e6a-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="39e6a-148"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="39e6a-149">IDL</span><span class="sxs-lookup"><span data-stu-id="39e6a-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39e6a-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39e6a-150"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="39e6a-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39e6a-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="39e6a-152"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39e6a-152"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
