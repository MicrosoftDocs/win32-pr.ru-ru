---
description: Функция-посредник для метода Креатедекодерфромстреам.
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: Функция IWICImagingFactory_CreateDecoderFromStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ab635d524adc379aae6d91cee5a65b41b39252bc60c7e260e5fe8158b5d47baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965173"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a>IWICImagingFactory \_ креатедекодерфромстреам \_ -функция

Функция-посредник для метода [**креатедекодерфромстреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*пистреам* \[ окне\]
</dt> <dd>

Тип: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***

Поток, из которого создается декодер.

</dd> <dt>

*пгуидвендор* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID**

Идентификатор GUID поставщика для декодера.

</dd> <dt>

*метадатаоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**Викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , используемый при создании декодера.

</dd> <dt>

*ппидекодер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Указатель, получающий указатель на новый [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), Windows \[ только классические приложения Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

