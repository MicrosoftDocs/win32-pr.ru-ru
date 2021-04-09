---
description: Возвращает интерфейсы расширения, которые могут поступать с драйвером устройства для получения образа Windows (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: Метод IWiaItem2::-Extension (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072775"
---
# <a name="iwiaitem2getextension-method"></a>Метод IWiaItem2:: Extension

Возвращает интерфейсы расширения, которые могут поступать с драйвером устройства для получения образа Windows (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*bstrName* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает имя расширения, на которое вызывающее приложение требует указатель на.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**сегментатионфилтер**


</dt> <dd>

Расширение фильтра сегментации. В настоящее время это допустимое значение для этого параметра.

</dd> </dl> </dd> <dt>

*риидекстенсионинтерфаце* \[ окне\]
</dt> <dd>

Тип: **рефиид**

Указывает идентификатор интерфейса расширения.

</dd> <dt>

*ппаут* \[ заполняет\]
</dt> <dd>

Тип: **void \* \***

Получает адрес указателя на интерфейс расширения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Приложение вызывает этот метод, чтобы создать объект расширения, реализующий один из интерфейсов расширения драйвера WIA 2,0. **IWiaItem2:: Extension** сохраняет адрес интерфейса расширения объекта расширения в параметре *риидекстенсионинтерфаце* . Затем приложение использует указатель интерфейса для вызова его методов.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *риидекстенсионинтерфаце* .

## <a name="examples"></a>Примеры

Креатесегментатионфилтер создает экземпляр фильтра сегментации драйвера ([**ивиасегментатионфилтер**](-wia-iwiasegmentationfilter.md)) путем вызова **IWiaItem2:: Extension** в переданном интерфейсе [**IWiaItem2**](-wia-iwiaitem2.md) .


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
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



 

 
