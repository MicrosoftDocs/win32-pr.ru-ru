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
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712619"
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

Тип: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_uiWidth * \[ в\]
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
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




