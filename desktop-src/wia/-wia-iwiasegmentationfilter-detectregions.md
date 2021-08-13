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
ms.openlocfilehash: 46496360d7b54bed837ba287d604233a9fac98ee13807744b4adbfb52e9934d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450264"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>Ивиасегментатионфилтер: метод:D Етектрегионс

Определяет подобласти изображения, расположенного на планшетном Платен, чтобы каждый из подрегионов можно было получить в отдельный элемент изображения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*пинпутстреам* \[ окне\]
</dt> <dd>

Тип: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Указывает указатель на изображение предварительной версии [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

*pWiaItem2* \[ окне\]
</dt> <dd>

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Указывает указатель на элемент [**IWiaItem2**](-wia-iwiaitem2.md) , для которого был получен *пинпутстреам* . Фильтр сегментации создает дочерние элементы для этого элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод определяет подобласти изображения, представленного Пинпутстреам. Для каждой подобласти, которую она обнаруживает, создается дочерний элемент для элемента [**IWiaItem2**](-wia-iwiaitem2.md) , указанного в параметре *pWiaItem2* . Для каждого дочернего элемента фильтр сегментации должен задавать значения для ограничивающего прямоугольника сканируемой области, используя следующие [**константы свойства элемента сканера WIA**](-wia-wiaitempropscanneritem.md).

-   [**\_кспос IP-адресов WIA \_**](-wia-wiaitempropscanneritem.md)
-   [**\_ИПОС IP-адресов WIA \_**](-wia-wiaitempropscanneritem.md)
-   [**\_ксекстент IP-адресов WIA \_**](-wia-wiaitempropscanneritem.md)
-   [**\_екстент IP-адресов WIA \_**](-wia-wiaitempropscanneritem.md)

Более расширенный фильтр может также требовать, чтобы другие [**константы свойств элементов сканера WIA**](-wia-wiaitempropscanneritem.md) , например **IP-адреса WIA, \_ \_ деравномерно \_** рассогласованы X и WIA, расменяли **\_ \_ \_ Y**, если драйвер поддерживает отмену наклона.

Если приложение вызывает **ивиасегментатионфилтер::D етектрегионс** несколько раз, приложение должно сначала удалить дочерние элементы, созданные при последнем вызове функции **Ивиасегментатионфилтер::D етектрегионс**.

Если приложение изменяет любые свойства в *pWiaItem2*, между получением изображения в *пинпутстреам* и его вызовом **ивиасегментатионфилтер::D етектрегионс**, исходные свойства (то есть свойства, которые элемент имел при получении потока) должны быть восстановлены. Это можно сделать с помощью [**жетпропертистреам**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) и [**сетпропертистреам**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).

Приложение должно сбросить [IStream](/windows/win32/api/objidl/nn-objidl-istream) , если его вызов передает один и тот же поток в фильтр сегментации более одного раза. Приложение также должно сбрасывать поток после первоначального скачивания и до вызова **ивиасегментатионфилтер::D етектрегионс**.

## <a name="examples"></a>Примеры

Сегментация выполняет обнаружение региона в потоке ( `pImageStream` ), переданном в детектсубрегионс. См. метод [**Extension**](-wia-iwiaitem2-getextension.md) для метода креатесегментатионфилтер, используемый в этом примере.


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



Довнлоадпревиевимаже скачивает данные изображения из сканера путем вызова метода [**жетневпревиев**](-wia-iwiapreview-getnewpreview.md) предварительной версии компонента. Затем он вызывает Детектсубрегионс, если пользователь приложения хочет вызвать фильтр сегментации, который создает дочерний элемент в pWiaItem2 для каждого обнаруженного региона. См. раздел **ивиасегментатионфилтер::D етектрегионс** для метода детектсубрегионс, используемого в этом примере.

В этом примере пользовательское приложение задается `m_bUseSegmentationFilter` путем щелчка флажка. Если приложение поддерживает это, сначала необходимо проверить, имеет ли драйвер фильтр сегментации, вызвав [**чеккекстенсион**](-wia-iwiaitem2-checkextension.md). См. [**жетневпревиев**](-wia-iwiapreview-getnewpreview.md) для примера метода чеккимгфилтер, в котором показано, как это можно сделать.


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
