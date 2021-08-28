---
description: IWICBitmapDecoder_GetThumbnail_Proxy функция-прокси для метода с параметром thumbnail.
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: Функция IWICBitmapDecoder_GetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d663ac34e74baf7b3f6f4476dde207b1ee05e81ff3bd47fe4b219f2f83efafca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592564"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a>\_ \_ Функция Ивикбитмапдекодер-эскиза

Функция-посредник для метода " [**thumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) ".

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

Указатель на этот объект [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*пписумбнаил* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***

Указатель, получающий указатель на [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) эскиза.

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



 

 




