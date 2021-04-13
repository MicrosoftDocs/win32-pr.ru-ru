---
description: Функция-посредник для метода Жетмиметипес.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: Функция IWICBitmapCodecInfo_GetMimeTypes_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541271"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a>ИвикбитмапкодеЦинфо \_ жетмиметипес \_ -функция

Функция-посредник для метода [**жетмиметипес**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Указатель на этот объект [_ *ивикбитмапкодеЦинфо* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*кчмиметипес* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера типов MIME.

</dd> <dt>

*взмиметипес* \[ заполняет\]
</dt> <dd>

Тип: **WCHAR \** _

Указатель, получающий типы MIME, связанные с кодеком.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Тип: **uint \** _

Фактический размер буфера, необходимый для получения всех типов MIME, связанных с кодеком.

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



 

 




