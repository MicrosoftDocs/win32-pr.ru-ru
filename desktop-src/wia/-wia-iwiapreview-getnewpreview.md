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
# <a name="iwiapreviewgetnewpreview-method"></a>Метод Ивиапревиев:: Жетневпревиев

Внутренне кэширует нефильтрованное изображение, возвращенное драйвером.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pWiaItem2* \[ окне\]
</dt> <dd>

Тип: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Указывает указатель на элемент [_ *IWiaItem2* *](-wia-iwiaitem2.md) для изображения.

</dd> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*пвиатрансферкаллбакк* \[ окне\]
</dt> <dd>

Тип: **[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _

Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* *](-wia-iwiatransfercallback.md) вызывающего приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Приложение должно вызвать **ивиапревиев:: жетневпревиев** перед вызовом [**Ивиапревиев::D етектрегионс**](-wia-iwiapreview-detectregions.md).

**Ивиапревиев:: жетневпревиев** задает свойство [**\_ \_ предварительной версии WIA DPS**](-wia-wiaitempropscannerdevice.md) (и сбрасывает его перед возвратом, если оно не было задано ранее). Это позволяет драйверу и оборудованию, а также фильтру обработки изображений известно, что элемент является предварительной проверкой.

На внутреннем этапе компонент предварительной версии для получения образа Windows (WIA) 2,0 создает экземпляр фильтра обработки изображений драйвера [**путем вызова метода**](-wia-iwiaitem2-getextension.md) *pWiaItem2*. Компонент WIA 2,0 Preview делает это, когда приложение вызывает **ивиапревиев:: жетневпревиев**. Компонент WIA 2,0 Preview также инициализирует фильтр в **ивиапревиев:: жетневпревиев**. Один и тот же экземпляр фильтра используется компонентом предварительной версии WIA 2,0 во время вызова [**ивиапревиев:: упдатепревиев**](-wia-iwiapreview-updatepreview.md).

Перед вызовом компонента предварительной версии WIA 2,0 приложение должно вызвать [**чеккекстенсион**](-wia-iwiaitem2-checkextension.md) , чтобы убедиться, что драйвер поставляется с фильтром обработки изображений. Он должен вызвать **чеккекстенсион** для элемента, который был бы передан **Ивиапревиев:: жетневпревиев**. Нет смысла предоставлять динамические предварительные версии без фильтра обработки изображений. Если приложение вызывает **ивиапревиев:: жетневпревиев** для драйвера без фильтра обработки изображений, вызов завершится ошибкой.

## <a name="examples"></a>Примеры

Чеккимгфилтер проверяет, имеет ли драйвер фильтр обработки изображений. Перед вызовом компонента предварительной версии приложение должно убедиться, что драйвер имеет фильтр обработки изображений.


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



Довнлоадпревиевимаже скачивает данные изображения из сканера, вызывая метод **ивиапревиев:: жетневпревиев** для предварительной версии компонента. Затем он вызывает Детектсубрегионс, если пользователь приложения хочет вызвать фильтр сегментации, который создает дочерний элемент в pWiaItem2 для каждого обнаруженного региона. См. раздел [**детектрегионс**](-wia-iwiasegmentationfilter-detectregions.md) для метода детектсубрегионс, используемого в этом примере.

В этом примере пользовательское приложение задается `m_bUseSegmentationFilter` путем щелчка флажка. Если приложение поддерживает это, сначала необходимо проверить, имеет ли драйвер фильтр сегментации, вызвав [**чеккекстенсион**](-wia-iwiaitem2-checkextension.md). См. **ивиапревиев:: жетневпревиев** в примере метода чеккимгфилтер, в котором показано, как это можно сделать.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




