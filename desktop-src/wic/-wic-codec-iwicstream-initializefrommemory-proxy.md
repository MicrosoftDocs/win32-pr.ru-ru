---
description: IWICStream_InitializeFromMemory_Proxy функция-прокси для метода Инитиализефроммемори.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: Функция IWICStream_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097132"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a>Ивикстреам \_ инитиализефроммемори \_ -функция

Функция-посредник для метода [**инитиализефроммемори**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***

Указатель на этот объект [**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .

</dd> <dt>

*пббуффер* \[ окне\]
</dt> <dd>

Тип: **Byte \***

Указатель на буфер, используемый для инициализации потока.

</dd> <dt>

*кббуфферсизе* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Размер буфера.

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



 

 




