---
description: Функция-посредник для метода "методом".
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: Функция IWICBitmapSource_GetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264873"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a>\_ \_ Функция прокси-сервера IWICBitmapSource с высоким разрешением

Функция-посредник для [**метода "**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) методом".

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Указатель на этот объект [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*пдпикс* \[ заполняет\]
</dt> <dd>

Тип: **Двойное \** _

Указатель, получающий разрешение dpi по оси x.

</dd> <dt>

_pDpiY * \[ out\]
</dt> <dd>

Тип: **Двойное \** _

Указатель, получающий разрешение dpi по оси y.

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



 

 




