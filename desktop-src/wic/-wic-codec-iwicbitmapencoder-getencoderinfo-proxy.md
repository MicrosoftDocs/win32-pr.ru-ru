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
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693762"
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

Тип: **[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _

Указатель на этот объект [_ *ивикбитмапенкодер* *](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .

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
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




