---
description: Функция-посредник для метода Креатебитмапфроммемори.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: Функция IWICImagingFactory_CreateBitmapFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e7f5567f2ead2b68440e448a9a03f36fdedceb5d31ecfc579f7df956988dfc01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033917"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>IWICImagingFactory \_ креатебитмапфроммемори \_ -функция

Функция-посредник для метода [**креатебитмапфроммемори**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
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

*кбстриде* \[ окне\]
</dt> <dd>

Тип: **uint**

[*Шаг*](/windows) с заданными данными пикселей.

</dd> <dt>

*кббуфферсизе* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер *пббуффер*.

</dd> <dt>

*пббуффер* \[ окне\]
</dt> <dd>

Тип: **Byte \***

Буфер, используемый для создания точечного рисунка.

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



 

