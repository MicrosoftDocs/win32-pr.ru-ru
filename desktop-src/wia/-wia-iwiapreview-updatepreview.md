---
description: 'Возвращает нефильтрованное изображение, кэшированное методом Ивиапревиев:: Жетневпревиев.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'Метод Ивиапревиев:: Упдатепревиев (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145403"
---
# <a name="iwiapreviewupdatepreview-method"></a><span data-ttu-id="46784-103">Метод Ивиапревиев:: Упдатепревиев</span><span class="sxs-lookup"><span data-stu-id="46784-103">IWiaPreview::UpdatePreview method</span></span>

<span data-ttu-id="46784-104">Возвращает нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="46784-104">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46784-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46784-105">Syntax</span></span>


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a><span data-ttu-id="46784-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="46784-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46784-107">*лоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46784-107">*lOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46784-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="46784-108">Type: **LONG**</span></span>

<span data-ttu-id="46784-109">Указывает, требует ли приложение компонент предварительной версии WIA 2,0 для передачи подобласти кэшированного изображения или всего кэшированного изображения в фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="46784-109">Specifies whether the application requires the WIA 2.0 Preview Component to pass a sub-region of the cached image or the entire cached image to the image processing filter.</span></span>

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span data-ttu-id="46784-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**виапревиевретурноригиналимаже**</span><span class="sxs-lookup"><span data-stu-id="46784-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span></span>


</dt> <dd>

<span data-ttu-id="46784-111">Передайте весь кэшированный образ в фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="46784-111">Pass the entire cached image to the image processing filter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="46784-112">*пчилдвиаитем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46784-112">*pChildWiaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46784-113">Тип: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="46784-113">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="46784-114">Задает указатель на элемент [_ *IWiaItem2* \*](-wia-iwiaitem2.md) , который является дочерним элементом элемента **IWiaItem2** , указанного параметром *pWiaItem2* метода [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="46784-114">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item, which is a child of the **IWiaItem2** item specified by the *pWiaItem2* parameter of the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="46784-115">Или, если приложению требуется предварительная версия всего планшета, указывает указатель на параметр *pWiaItem2* метода **Ивиапревиев:: жетневпревиев** .</span><span class="sxs-lookup"><span data-stu-id="46784-115">Or, if the application requires a preview of the whole flatbed, specifies a pointer to the *pWiaItem2* parameter of the **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="46784-116">Если *пчилдвиаитем* является дочерним параметром **Ивиапревиев:: жетневпревиев** *pWiaItem2* , этот дочерний элемент обычно создается фильтром сегментации.</span><span class="sxs-lookup"><span data-stu-id="46784-116">When *pChildWiaItem* is a child of **IWiaPreview::GetNewPreview**'s *pWiaItem2* parameter, this child item is typically created by the segmentation filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46784-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46784-117">Return value</span></span>

<span data-ttu-id="46784-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46784-118">Type: **HRESULT**</span></span>

<span data-ttu-id="46784-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="46784-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46784-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46784-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46784-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46784-121">Remarks</span></span>

<span data-ttu-id="46784-122">Этот метод передает кэшированное нефильтрованное изображение с помощью фильтра обработки изображений, который затем записывает отфильтрованные данные в поток, предоставленный приложением.</span><span class="sxs-lookup"><span data-stu-id="46784-122">This method passes the cached, unfiltered image through the image processing filter, which then writes the filtered data to the application-provided stream.</span></span> <span data-ttu-id="46784-123">Компонент WIA 2,0 Preview извлекает этот поток, вызывая метод [**жетнекстстреам**](-wia-iwiatransfercallback-getnextstream.md) фильтра обработки изображений, который затем вызывает реализацию **жетнекстстреам** обратного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="46784-123">The WIA 2.0 Preview Component retrieves this stream by calling the image processing filter's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method, which then calls the application callback's **GetNextStream** implementation.</span></span> <span data-ttu-id="46784-124">Перед вызовом **ивиапревиев:: упдатепревиев** приложение должно сначала вызвать [**Ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) , чтобы получить изображение из сканера. в противном случае метод возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="46784-124">Before calling **IWiaPreview::UpdatePreview**, an application must first call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) to acquire the image from the scanner; otherwise, the method returns an error.</span></span>

<span data-ttu-id="46784-125">Компонент WIA 2,0 Preview хранит нефильтрованное изображение, загруженное из драйвера.</span><span class="sxs-lookup"><span data-stu-id="46784-125">The WIA 2.0 Preview Component stores the unfiltered image downloaded from the driver.</span></span> <span data-ttu-id="46784-126">Возможно, элемент WIA 2,0, переданный в **ивиапревиев:: упдатепревиев** , представляет только небольшой регион изображения, скачанного из драйвера.</span><span class="sxs-lookup"><span data-stu-id="46784-126">It is possible that the WIA 2.0 item passed into **IWiaPreview::UpdatePreview** represents only a small region of the image downloaded from the driver.</span></span> <span data-ttu-id="46784-127">Если это так, компонент предварительной версии WIA 2,0 фактически вырезает этот регион из кэшированного образа, прежде чем передать его в фильтр обработки изображений, который, в свою очередь, передает данные отфильтрованного изображения обратно в приложение.</span><span class="sxs-lookup"><span data-stu-id="46784-127">If this is the case the WIA 2.0 Preview Component actually cuts out this region from the cached image before it passes it to the image processing filter, which in turn passes the filtered image data back to the application.</span></span>

<span data-ttu-id="46784-128">Чтобы приложение передавало весь кэшированный образ в фильтр обработки изображений (который, в свою очередь, передает его в приложение), он должен установить для *лоптионс* значение **виапревиевретурноригиналимаже** при вызове **ивиапревиев:: упдатепревиев**.</span><span class="sxs-lookup"><span data-stu-id="46784-128">For an application to pass the entire cached image to the image processing filter (which in turn passes it to the application), it must set the *lOptions* to **WiaPreviewReturnOriginalImage** when calling **IWiaPreview::UpdatePreview**.</span></span> <span data-ttu-id="46784-129">При установке *лоптионс* в **виапревиевретурноригиналимаже** приложение должно гарантировать, что параметры экстента ([**WIA- \_ адреса \_ ксекстент**](-wia-wiaitempropscanneritem.md) и **WIA-пакетов \_ \_ екстент**) элемента, переданного в **ивиапревиев:: упдатепревиев** , соответствует полному кэшированному изображению.</span><span class="sxs-lookup"><span data-stu-id="46784-129">When setting *lOptions* to **WiaPreviewReturnOriginalImage**, the application must ensure that the extent settings ([**WIA\_IPS\_XEXTENT**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YEXTENT**) of the item passed into **IWiaPreview::UpdatePreview** matches the full-cached image.</span></span> <span data-ttu-id="46784-130">В этом случае фильтр обработки изображений не должен выполнять никаких других действий. Он просто фильтрует изображение на основе свойств *пчилдвиаитем* (обычно в данном случае *пчилдвиаитем* — тот же элемент, который был передан в [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md)).</span><span class="sxs-lookup"><span data-stu-id="46784-130">The image processing filter need not do anything different in this case; it simply filters the image, based on the properties of *pChildWiaItem* (typically in this case *pChildWiaItem* is the same item that was passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span></span> <span data-ttu-id="46784-131">Разные подобласти игнорируются, и весь образ фильтруется с использованием одних и тех же параметров.</span><span class="sxs-lookup"><span data-stu-id="46784-131">The different sub-regions are ignored and the whole image is filtered using the same settings.</span></span> <span data-ttu-id="46784-132">Существует несколько причин, по которым приложение сделает это.</span><span class="sxs-lookup"><span data-stu-id="46784-132">There are a couple of reasons why an application would do this.</span></span>

1.  <span data-ttu-id="46784-133">Приложение может не поддерживать изменение параметров (таких как [**\_ \_ яркость IP-адресов**](-wia-wiaitempropscanneritem.md) и **\_ \_ контрастные IP-адреса**) по отдельности для каждого региона, который обнаруживает фильтр сегментации (или может даже не использовать фильтр сегментации).</span><span class="sxs-lookup"><span data-stu-id="46784-133">The application may not support changing the settings (like [**WIA\_IPS\_BRIGHTNESS**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_CONTRAST**) individually for each region that the segmentation filter detects (or it may not even want to use the segmentation filter).</span></span> <span data-ttu-id="46784-134">Приложению проще вызывать **ивиапревиев:: упдатепревиев** с **виапревиевретурноригиналимаже** , чтобы он всегда получал полный образ из компонента предварительной версии WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="46784-134">It is easier for the application to call **IWiaPreview::UpdatePreview** with **WiaPreviewReturnOriginalImage** so that it always receives the full image from the WIA 2.0 Preview Component.</span></span>
2.  <span data-ttu-id="46784-135">Компонент предварительной версии WIA 2,0 не поддерживает формат изображения для предварительного просмотра изображения. в этом случае невозможно выполнить действия для вырезания нужного региона.</span><span class="sxs-lookup"><span data-stu-id="46784-135">The WIA 2.0 Preview Component does not support the image format of the preview image, in which case it cannot perform the actions to cut out the desired region.</span></span> <span data-ttu-id="46784-136">Формат изображения компонента WIA 2,0 Preview ограничен форматами, для которых существуют кодировщики и декодеры Windows GDI+ 1,1.</span><span class="sxs-lookup"><span data-stu-id="46784-136">The WIA 2.0 Preview Component's image format support is limited to formats for which there are Windows GDI+ 1.1 encoders and decoders.</span></span> <span data-ttu-id="46784-137">Эти форматы являются точечными рисунками (BMP) (точечный рисунок, включающий БИТМАПФИЛЕХЕАДЕР), формат GIF, JPEG, PNG и формат файла изображения с тегами (TIFF).</span><span class="sxs-lookup"><span data-stu-id="46784-137">These formats are bitmap (BMP) (a bitmap that includes the BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="46784-138">Обратите внимание, что если приложение передает **виапревиевретурноригиналимаже** в **Ивиапревиев:: УПДАТЕПРЕВИЕВ**, компонент WIA 2,0 Preview может поддерживать любое изображение или формат пикселей.</span><span class="sxs-lookup"><span data-stu-id="46784-138">Note that if the application passes **WiaPreviewReturnOriginalImage** into **IWiaPreview::UpdatePreview**, the WIA 2.0 Preview Component can support any image or pixel format.</span></span>

<span data-ttu-id="46784-139">**Ивиапревиев:: упдатепревиев** задает свойство [**\_ \_ предварительной версии WIA DPS**](-wia-wiaitempropscannerdevice.md) (и сбрасывает его перед возвратом, если оно не было задано ранее).</span><span class="sxs-lookup"><span data-stu-id="46784-139">**IWiaPreview::UpdatePreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="46784-140">Это позволяет драйверу (и оборудованию), а также фильтру обработки изображений, известно, что элемент является предварительной проверкой.</span><span class="sxs-lookup"><span data-stu-id="46784-140">This lets the driver (and hardware) as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="46784-141">Приложение должно гарантировать, что *пчилдвиаитем* имеет тот же формат изображения ([**\_ \_ Формат WIA IPA**](-wia-wiaitempropcommonitem.md)) и разрешение (с помощью пакетов [**WIA \_ \_ ксрес**](-wia-wiaitempropscanneritem.md) и **WIA- \_ адресов \_ ирес**), так как *пвиаитем* был передан в [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="46784-141">An application must ensure that *pChildWiaItem* has the same image format ([**WIA\_IPA\_FORMAT**](-wia-wiaitempropcommonitem.md)) and resolution ([**WIA\_IPS\_XRES**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YRES**) as *pWiaItem* had when it was passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="46784-142">Формат дочернего элемента должен соответствовать формату кэшированного образа компонента WIA 2,0 Preview (компонент WIA 2,0 Preview не выполняет преобразование изображения).</span><span class="sxs-lookup"><span data-stu-id="46784-142">The format of the child item must correspond to the format of the WIA 2.0 Preview Component's cached image (the WIA 2.0 Preview Component performs no image conversion).</span></span>

## <a name="examples"></a><span data-ttu-id="46784-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="46784-143">Examples</span></span>

<span data-ttu-id="46784-144">Упдатерегион должен вызываться каждый раз, когда пользователь изменяет, например, яркость или контраст для дочернего элемента, представленного `dwRegionNumber` .</span><span class="sxs-lookup"><span data-stu-id="46784-144">UpdateRegion should be called each time a user changes, for example, the brightness or contrast for the child item represented by `dwRegionNumber`.</span></span> <span data-ttu-id="46784-145">Этот дочерний элемент ранее был создан фильтром сегментации ([**ивиасегментатионфилтер**](-wia-iwiasegmentationfilter.md).</span><span class="sxs-lookup"><span data-stu-id="46784-145">This child item has previously been created by the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span></span> <span data-ttu-id="46784-146">Образ, записанный в [IStream](/windows/win32/api/objidl/nn-objidl-istream) , возвращается методом [**жетнекстстреам**](-wia-iwiatransfercallback-getnextstream.md) интерфейса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="46784-146">The image written to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) is returned by the transfer callback interface's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method.</span></span> <span data-ttu-id="46784-147">В этом примере код для Жетсубрегионитем опущен.</span><span class="sxs-lookup"><span data-stu-id="46784-147">The code for GetSubRegionItem is omitted in this example.</span></span>

<span data-ttu-id="46784-148">После вызова этой функции приложение обычно перерисовывает область на экране.</span><span class="sxs-lookup"><span data-stu-id="46784-148">After this function has been called, an application would typically redraw the region on the screen.</span></span>


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a><span data-ttu-id="46784-149">Требования</span><span class="sxs-lookup"><span data-stu-id="46784-149">Requirements</span></span>



| <span data-ttu-id="46784-150">Требование</span><span class="sxs-lookup"><span data-stu-id="46784-150">Requirement</span></span> | <span data-ttu-id="46784-151">Значение</span><span class="sxs-lookup"><span data-stu-id="46784-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46784-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46784-152">Minimum supported client</span></span><br/> | <span data-ttu-id="46784-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46784-153">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="46784-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46784-154">Minimum supported server</span></span><br/> | <span data-ttu-id="46784-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46784-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="46784-156">Header</span><span class="sxs-lookup"><span data-stu-id="46784-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="46784-157"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="46784-157"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="46784-158">IDL</span><span class="sxs-lookup"><span data-stu-id="46784-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46784-159"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46784-159"><dt>Wia.idl</dt></span></span> </dl> |



 

 
