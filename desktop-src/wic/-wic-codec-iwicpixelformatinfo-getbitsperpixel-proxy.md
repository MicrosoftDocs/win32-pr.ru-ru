---
description: Функция-посредник для метода Жетбитсперпиксел.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: Функция IWICPixelFormatInfo_GetBitsPerPixel_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d53cf904242843ed57661a3bf0b1efb864513d53417b2ed09437567e56364ac8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393564"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a>Ивикпикселформатинфо \_ жетбитсперпиксел \_ -функция

Функция-посредник для метода [**жетбитсперпиксел**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Указатель на этот объект [**ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .

</dd> <dt>

*пуибитсперпиксел* \[ заполняет\]
</dt> <dd>

Тип: **uint \***

Указатель, получающий пиксель формата пикселей.

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



 

 




