---
description: Функция-посредник для метода Креатедекодерфромфилехандле.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: Функция IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998704"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a>IWICImagingFactory \_ креатедекодерфромфилехандле \_ -функция

Функция-посредник для метода [**креатедекодерфромфилехандле**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hFile * \[ в\]
</dt> <dd>

Тип: **ulong \_ ptr**

Описатель файла, из которого создается декодер.

</dd> <dt>

*пгуидвендор* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID* _

Идентификатор GUID поставщика для декодера.

</dd> <dt>

_metadataOptions * \[ в\]
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
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




