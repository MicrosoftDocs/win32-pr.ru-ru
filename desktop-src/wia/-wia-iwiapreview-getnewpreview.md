---
description: Внутренне кэширует нефильтрованное изображение, возвращенное драйвером.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'Метод Ивиапревиев:: Жетневпревиев (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711095"
---
# <a name="iwiapreviewgetnewpreview-method"></a><span data-ttu-id="0cd83-103">Метод Ивиапревиев:: Жетневпревиев</span><span class="sxs-lookup"><span data-stu-id="0cd83-103">IWiaPreview::GetNewPreview method</span></span>

<span data-ttu-id="0cd83-104">Внутренне кэширует нефильтрованное изображение, возвращенное драйвером.</span><span class="sxs-lookup"><span data-stu-id="0cd83-104">Caches internally the unfiltered image returned from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd83-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cd83-105">Syntax</span></span>


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="0cd83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cd83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cd83-107">*pWiaItem2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0cd83-107">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-108">Тип: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="0cd83-108">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="0cd83-109">Указывает указатель на элемент [_ *IWiaItem2* \*](-wia-iwiaitem2.md) для изображения.</span><span class="sxs-lookup"><span data-stu-id="0cd83-109">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for the image.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-110">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0cd83-110">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-111">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="0cd83-111">Type: **LONG**</span></span>

<span data-ttu-id="0cd83-112">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="0cd83-112">Currently unused.</span></span> <span data-ttu-id="0cd83-113">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="0cd83-113">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0cd83-114">*пвиатрансферкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0cd83-114">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cd83-115">Тип: \**[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="0cd83-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="0cd83-116">Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* \*](-wia-iwiatransfercallback.md) вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="0cd83-116">Specifies a pointer to the calling application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cd83-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cd83-117">Return value</span></span>

<span data-ttu-id="0cd83-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0cd83-118">Type: **HRESULT**</span></span>

<span data-ttu-id="0cd83-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0cd83-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0cd83-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cd83-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cd83-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0cd83-121">Remarks</span></span>

<span data-ttu-id="0cd83-122">Приложение должно вызвать **ивиапревиев:: жетневпревиев** перед вызовом [**Ивиапревиев::D етектрегионс**](-wia-iwiapreview-detectregions.md).</span><span class="sxs-lookup"><span data-stu-id="0cd83-122">An application must call **IWiaPreview::GetNewPreview** before it calls [**IWiaPreview::DetectRegions**](-wia-iwiapreview-detectregions.md).</span></span>

<span data-ttu-id="0cd83-123">**Ивиапревиев:: жетневпревиев** задает свойство [**\_ \_ предварительной версии WIA DPS**](-wia-wiaitempropscannerdevice.md) (и сбрасывает его перед возвратом, если оно не было задано ранее).</span><span class="sxs-lookup"><span data-stu-id="0cd83-123">**IWiaPreview::GetNewPreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="0cd83-124">Это позволяет драйверу и оборудованию, а также фильтру обработки изображений известно, что элемент является предварительной проверкой.</span><span class="sxs-lookup"><span data-stu-id="0cd83-124">This lets the driver and hardware, as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="0cd83-125">На внутреннем этапе компонент предварительной версии для получения образа Windows (WIA) 2,0 создает экземпляр фильтра обработки изображений драйвера [**путем вызова метода**](-wia-iwiaitem2-getextension.md) *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="0cd83-125">Internally, the Windows Image Acquisition (WIA) 2.0 preview component creates an instance of the driver's image processing filter by calling [**GetExtension**](-wia-iwiaitem2-getextension.md) on *pWiaItem2*.</span></span> <span data-ttu-id="0cd83-126">Компонент WIA 2,0 Preview делает это, когда приложение вызывает **ивиапревиев:: жетневпревиев**.</span><span class="sxs-lookup"><span data-stu-id="0cd83-126">The WIA 2.0 preview component does this when the application calls **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="0cd83-127">Компонент WIA 2,0 Preview также инициализирует фильтр в **ивиапревиев:: жетневпревиев**.</span><span class="sxs-lookup"><span data-stu-id="0cd83-127">The WIA 2.0 preview component also initializes the filter in **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="0cd83-128">Один и тот же экземпляр фильтра используется компонентом предварительной версии WIA 2,0 во время вызова [**ивиапревиев:: упдатепревиев**](-wia-iwiapreview-updatepreview.md).</span><span class="sxs-lookup"><span data-stu-id="0cd83-128">The same filter instance is used by the WIA 2.0 preview component during a call to [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span></span>

<span data-ttu-id="0cd83-129">Перед вызовом компонента предварительной версии WIA 2,0 приложение должно вызвать [**чеккекстенсион**](-wia-iwiaitem2-checkextension.md) , чтобы убедиться, что драйвер поставляется с фильтром обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="0cd83-129">Before calling into the WIA 2.0 preview component, an application should call [**CheckExtension**](-wia-iwiaitem2-checkextension.md) to make sure that the driver comes with an image processing filter.</span></span> <span data-ttu-id="0cd83-130">Он должен вызвать **чеккекстенсион** для элемента, который был бы передан **Ивиапревиев:: жетневпревиев**.</span><span class="sxs-lookup"><span data-stu-id="0cd83-130">It should call **CheckExtension** on the item that it would pass to **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="0cd83-131">Нет смысла предоставлять динамические предварительные версии без фильтра обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="0cd83-131">It is useless to provide live previews without an image processing filter.</span></span> <span data-ttu-id="0cd83-132">Если приложение вызывает **ивиапревиев:: жетневпревиев** для драйвера без фильтра обработки изображений, вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="0cd83-132">If an application calls **IWiaPreview::GetNewPreview** for a driver without an image processing filter, the call will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="0cd83-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="0cd83-133">Examples</span></span>

<span data-ttu-id="0cd83-134">Чеккимгфилтер проверяет, имеет ли драйвер фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="0cd83-134">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="0cd83-135">Перед вызовом компонента предварительной версии приложение должно убедиться, что драйвер имеет фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="0cd83-135">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



<span data-ttu-id="0cd83-136">Довнлоадпревиевимаже скачивает данные изображения из сканера, вызывая метод **ивиапревиев:: жетневпревиев** для предварительной версии компонента.</span><span class="sxs-lookup"><span data-stu-id="0cd83-136">DownloadPreviewImage downloads image data from the scanner by calling the preview component's **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="0cd83-137">Затем он вызывает Детектсубрегионс, если пользователь приложения хочет вызвать фильтр сегментации, который создает дочерний элемент в pWiaItem2 для каждого обнаруженного региона.</span><span class="sxs-lookup"><span data-stu-id="0cd83-137">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="0cd83-138">См. раздел [**детектрегионс**](-wia-iwiasegmentationfilter-detectregions.md) для метода детектсубрегионс, используемого в этом примере.</span><span class="sxs-lookup"><span data-stu-id="0cd83-138">See [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="0cd83-139">В этом примере пользовательское приложение задается `m_bUseSegmentationFilter` путем щелчка флажка.</span><span class="sxs-lookup"><span data-stu-id="0cd83-139">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="0cd83-140">Если приложение поддерживает это, сначала необходимо проверить, имеет ли драйвер фильтр сегментации, вызвав [**чеккекстенсион**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="0cd83-140">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="0cd83-141">См. **ивиапревиев:: жетневпревиев** в примере метода чеккимгфилтер, в котором показано, как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="0cd83-141">See **IWiaPreview::GetNewPreview** for the CheckImgFilter method example that shows how this can be done.</span></span>


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0cd83-142">Требования</span><span class="sxs-lookup"><span data-stu-id="0cd83-142">Requirements</span></span>



| <span data-ttu-id="0cd83-143">Требование</span><span class="sxs-lookup"><span data-stu-id="0cd83-143">Requirement</span></span> | <span data-ttu-id="0cd83-144">Значение</span><span class="sxs-lookup"><span data-stu-id="0cd83-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd83-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cd83-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd83-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0cd83-146">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0cd83-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cd83-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd83-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0cd83-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0cd83-149">Header</span><span class="sxs-lookup"><span data-stu-id="0cd83-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cd83-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cd83-150"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cd83-151">IDL</span><span class="sxs-lookup"><span data-stu-id="0cd83-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cd83-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cd83-152"><dt>Wia.idl</dt></span></span> </dl> |



 

 




