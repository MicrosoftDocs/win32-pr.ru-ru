---
description: IWICBitmapSource_CopyPalette_Proxy функция-прокси для метода Копипалетте.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: Функция IWICBitmapSource_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 42049a143d749398d849f709959ac6a99fe5789e52be0a59dfb9fe55019eb533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812294"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a>IWICBitmapSource \_ копипалетте \_ -функция

Функция-посредник для метода [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Указатель на этот объект [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*пипалетте* \[ окне\]
</dt> <dd>

Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Палитра.

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



 

 




