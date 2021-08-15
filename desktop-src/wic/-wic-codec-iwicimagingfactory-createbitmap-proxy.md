---
description: Функция-посредник для метода Креатебитмап.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: Функция IWICImagingFactory_CreateBitmap_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978946b5c22d8e4cb3427dbf27e5bb745efde259b48811a2b2a82e3721108184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965203"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a>IWICImagingFactory \_ креатебитмап \_ -функция

Функция-посредник для метода [**креатебитмап**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*уивидс* \[ окне\]
</dt> <dd>

Тип: **uint**

Ширина нового растрового изображения.

</dd> <dt>

*уихеигхт* \[ окне\]
</dt> <dd>

Тип: **uint**

Высота нового растрового изображения.

</dd> <dt>

*PixelFormat* \[ окне\]
</dt> <dd>

Тип: **рефвикпикселформатгуид**

Формат пикселей нового растрового изображения.

</dd> <dt>

*параметр* \[ окне\]
</dt> <dd>

Тип: **[ **викбитмапкреатекачеоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Параметры создания кэша нового растрового изображения.

</dd> <dt>

*ппибитмап* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Указатель, получающий указатель на новое растровое изображение.

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



 

 




