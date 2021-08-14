---
description: Функция-посредник для метода Жетенкодеринфо.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: Функция IWICBitmapEncoder_GetEncoderInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b423c5efb1dc4db386c5a77b15e5dabc07e05c7c740ccbc4ab411111122f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207215"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a>Ивикбитмапенкодер \_ жетенкодеринфо \_ -функция

Функция-посредник для метода [**жетенкодеринфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Указатель на этот объект [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .

</dd> <dt>

*ппиенкодеринфо* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикбитмапенкодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***

Указатель, получающий указатель на [**ивикбитмапенкодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).

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



 

 




