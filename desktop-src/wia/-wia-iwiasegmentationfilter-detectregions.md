---
description: Определяет подобласти изображения, расположенного на планшетном Платен, чтобы каждый из подрегионов можно было получить в отдельный элемент изображения.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: 'Ивиасегментатионфилтер: метод:D Етектрегионс (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145400"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a><span data-ttu-id="4bffd-103">Ивиасегментатионфилтер: метод:D Етектрегионс</span><span class="sxs-lookup"><span data-stu-id="4bffd-103">IWiaSegmentationFilter::DetectRegions method</span></span>

<span data-ttu-id="4bffd-104">Определяет подобласти изображения, расположенного на планшетном Платен, чтобы каждый из подрегионов можно было получить в отдельный элемент изображения.</span><span class="sxs-lookup"><span data-stu-id="4bffd-104">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bffd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bffd-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="4bffd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bffd-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4bffd-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bffd-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="4bffd-108">Type: **LONG**</span></span>

<span data-ttu-id="4bffd-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="4bffd-109">Currently unused.</span></span> <span data-ttu-id="4bffd-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4bffd-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4bffd-111">*пинпутстреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4bffd-111">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bffd-112">Тип: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="4bffd-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="4bffd-113">Указывает указатель на изображение предварительной версии [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="4bffd-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview image.</span></span>

</dd> <dt>

<span data-ttu-id="4bffd-114">_pWiaItem2 \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4bffd-114">_pWiaItem2\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bffd-115">Тип: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="4bffd-115">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="4bffd-116">Указывает указатель на элемент [_ *IWiaItem2* \*](-wia-iwiaitem2.md) , для которого был получен *пинпутстреам* .</span><span class="sxs-lookup"><span data-stu-id="4bffd-116">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for which *pInputStream* was acquired.</span></span> <span data-ttu-id="4bffd-117">Фильтр сегментации создает дочерние элементы для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="4bffd-117">The segmentation filter creates child items for this item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bffd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bffd-118">Return value</span></span>

<span data-ttu-id="4bffd-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4bffd-119">Type: **HRESULT**</span></span>

<span data-ttu-id="4bffd-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4bffd-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bffd-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4bffd-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bffd-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bffd-122">Remarks</span></span>

<span data-ttu-id="4bffd-123">Этот метод определяет подобласти изображения, представленного Пинпутстреам.</span><span class="sxs-lookup"><span data-stu-id="4bffd-123">This method determines the sub-regions of the image represented by pInputStream.</span></span> <span data-ttu-id="4bffd-124">Для каждой подобласти, которую она обнаруживает, создается дочерний элемент для элемента [**IWiaItem2**](-wia-iwiaitem2.md) , указанного в параметре *pWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="4bffd-124">For each sub-region that it detects, it creates a child item for the [**IWiaItem2**](-wia-iwiaitem2.md) item specified in the *pWiaItem2* parameter.</span></span> <span data-ttu-id="4bffd-125">Для каждого дочернего элемента фильтр сегментации должен задавать значения для ограничивающего прямоугольника сканируемой области, используя следующие [**константы свойства элемента сканера WIA**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="4bffd-125">For each child item, the segmentation filter must set values for the bounding rectangle of the area to scan, using the following [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

-   [<span data-ttu-id="4bffd-126">**\_кспос IP-адресов WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4bffd-126">**WIA\_IPS\_XPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="4bffd-127">**\_ИПОС IP-адресов WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4bffd-127">**WIA\_IPS\_YPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="4bffd-128">**\_ксекстент IP-адресов WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4bffd-128">**WIA\_IPS\_XEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="4bffd-129">**\_екстент IP-адресов WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4bffd-129">**WIA\_IPS\_YEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)

<span data-ttu-id="4bffd-130">Более расширенный фильтр может также требовать, чтобы другие [**константы свойств элементов сканера WIA**](-wia-wiaitempropscanneritem.md) , например **IP-адреса WIA, \_ \_ деравномерно \_** рассогласованы X и WIA, расменяли **\_ \_ \_ Y**, если драйвер поддерживает отмену наклона.</span><span class="sxs-lookup"><span data-stu-id="4bffd-130">A more advanced filter may also require other [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md) such as **WIA\_IPS\_DESKEW\_X** and **WIA\_IPS\_DESKEW\_Y**, if the driver supports de-skewing.</span></span>

<span data-ttu-id="4bffd-131">Если приложение вызывает **ивиасегментатионфилтер::D етектрегионс** несколько раз, приложение должно сначала удалить дочерние элементы, созданные при последнем вызове функции **Ивиасегментатионфилтер::D етектрегионс**.</span><span class="sxs-lookup"><span data-stu-id="4bffd-131">If the application calls **IWiaSegmentationFilter::DetectRegions** more than once, the application must first delete the child items created by the last call to **IWiaSegmentationFilter::DetectRegions**.</span></span>

<span data-ttu-id="4bffd-132">Если приложение изменяет любые свойства в *pWiaItem2*, между получением изображения в *пинпутстреам* и его вызовом **ивиасегментатионфилтер::D етектрегионс**, исходные свойства (то есть свойства, которые элемент имел при получении потока) должны быть восстановлены.</span><span class="sxs-lookup"><span data-stu-id="4bffd-132">If an application changes any properties into *pWiaItem2*, between acquiring the image into *pInputStream* and its call to **IWiaSegmentationFilter::DetectRegions**, the original properties (that is, the properties the item had when the stream was acquired) must be restored.</span></span> <span data-ttu-id="4bffd-133">Это можно сделать с помощью [**жетпропертистреам**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) и [**сетпропертистреам**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span><span class="sxs-lookup"><span data-stu-id="4bffd-133">This can be done by [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span></span>

<span data-ttu-id="4bffd-134">Приложение должно сбросить [IStream](/windows/win32/api/objidl/nn-objidl-istream) , если его вызов передает один и тот же поток в фильтр сегментации более одного раза.</span><span class="sxs-lookup"><span data-stu-id="4bffd-134">The application must reset the [IStream](/windows/win32/api/objidl/nn-objidl-istream) if its call passes the same stream into the segmentation filter more than once.</span></span> <span data-ttu-id="4bffd-135">Приложение также должно сбрасывать поток после первоначального скачивания и до вызова **ивиасегментатионфилтер::D етектрегионс**.</span><span class="sxs-lookup"><span data-stu-id="4bffd-135">The application must also reset the stream after the initial download and before calling **IWiaSegmentationFilter::DetectRegions**.</span></span>

## <a name="examples"></a><span data-ttu-id="4bffd-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="4bffd-136">Examples</span></span>

<span data-ttu-id="4bffd-137">Сегментация выполняет обнаружение региона в потоке ( `pImageStream` ), переданном в детектсубрегионс.</span><span class="sxs-lookup"><span data-stu-id="4bffd-137">The segmentation performs region detection on the stream (`pImageStream`) passed into DetectSubregions.</span></span> <span data-ttu-id="4bffd-138">См. метод [**Extension**](-wia-iwiaitem2-getextension.md) для метода креатесегментатионфилтер, используемый в этом примере.</span><span class="sxs-lookup"><span data-stu-id="4bffd-138">See the [**GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter method used in this example.</span></span>


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



<span data-ttu-id="4bffd-139">Довнлоадпревиевимаже скачивает данные изображения из сканера путем вызова метода [**жетневпревиев**](-wia-iwiapreview-getnewpreview.md) предварительной версии компонента.</span><span class="sxs-lookup"><span data-stu-id="4bffd-139">DownloadPreviewImage downloads image data from the scanner by calling the preview component's [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="4bffd-140">Затем он вызывает Детектсубрегионс, если пользователь приложения хочет вызвать фильтр сегментации, который создает дочерний элемент в pWiaItem2 для каждого обнаруженного региона.</span><span class="sxs-lookup"><span data-stu-id="4bffd-140">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="4bffd-141">См. раздел **ивиасегментатионфилтер::D етектрегионс** для метода детектсубрегионс, используемого в этом примере.</span><span class="sxs-lookup"><span data-stu-id="4bffd-141">See **IWiaSegmentationFilter::DetectRegions** for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="4bffd-142">В этом примере пользовательское приложение задается `m_bUseSegmentationFilter` путем щелчка флажка.</span><span class="sxs-lookup"><span data-stu-id="4bffd-142">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="4bffd-143">Если приложение поддерживает это, сначала необходимо проверить, имеет ли драйвер фильтр сегментации, вызвав [**чеккекстенсион**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="4bffd-143">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="4bffd-144">См. [**жетневпревиев**](-wia-iwiapreview-getnewpreview.md) для примера метода чеккимгфилтер, в котором показано, как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="4bffd-144">See [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) for the CheckImgFilter method example that shows how this can be done.</span></span>


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
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
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
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="4bffd-145">Требования</span><span class="sxs-lookup"><span data-stu-id="4bffd-145">Requirements</span></span>



| <span data-ttu-id="4bffd-146">Требование</span><span class="sxs-lookup"><span data-stu-id="4bffd-146">Requirement</span></span> | <span data-ttu-id="4bffd-147">Значение</span><span class="sxs-lookup"><span data-stu-id="4bffd-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4bffd-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bffd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4bffd-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4bffd-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4bffd-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bffd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4bffd-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4bffd-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4bffd-152">Header</span><span class="sxs-lookup"><span data-stu-id="4bffd-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bffd-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bffd-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bffd-154">IDL</span><span class="sxs-lookup"><span data-stu-id="4bffd-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4bffd-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4bffd-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 
