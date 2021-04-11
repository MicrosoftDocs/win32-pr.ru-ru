---
description: Функция-посредник для метода Жетфиликстенсионс.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: Функция IWICBitmapCodecInfo_GetFileExtensions_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343232"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a>ИвикбитмапкодеЦинфо \_ жетфиликстенсионс \_ -функция

Функция-посредник для метода [**жетфиликстенсионс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Указатель на этот объект [_ *ивикбитмапкодеЦинфо* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*кчфиликстенсионс* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера расширения имени файла.

</dd> <dt>

*взфиликстенсионс* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \** _

Указатель, получающий расширения имен файлов, связанные с кодеком.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Тип: **uint \** _

Фактический размер буфера, необходимый для получения всех расширений имен файлов, связанных с кодеком.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




