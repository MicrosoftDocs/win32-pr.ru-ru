---
description: IWICBitmapDecoder_CopyPalette_Proxy функция-прокси для метода Копипалетте.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: Функция IWICBitmapDecoder_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff4d856f1bfae331bf4c2442ac01ce4742810ba4ac3e0f4c3a8a067fddd4360a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965383"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a>Ивикбитмапдекодер \_ копипалетте \_ -функция

Функция-посредник для метода [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

Указатель на этот объект [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*пипалетте* \[ окне\]
</dt> <dd>

Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Копируемая палитра изображений.

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



 

 




