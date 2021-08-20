---
description: Функция-посредник для метода NOFRAMES.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: Функция IWICBitmapDecoder_GetFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0301501e39e85d05b83b132bfbee38a5157bd61f227f154ab7a020770e1b22ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034123"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a>\_ \_ Функция прокси-сервера ивикбитмапдекодер NOFRAMES

Функция-посредник для метода [**noframes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

Указатель на этот объект [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*индекс* \[ окне\]
</dt> <dd>

Тип: **uint**

Определенный кадр для извлечения.

</dd> <dt>

*ппибитмапфраме* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***

Указатель, получающий указатель на [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).

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



 

 




