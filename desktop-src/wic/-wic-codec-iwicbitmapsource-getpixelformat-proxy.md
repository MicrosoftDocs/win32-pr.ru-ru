---
description: Функция-посредник для метода Жетпикселформат.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: Функция IWICBitmapSource_GetPixelFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702400"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a>IWICBitmapSource \_ жетпикселформат \_ -функция

Функция-посредник для метода [**жетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Указатель на этот объект [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*ппикселформат* \[ заполняет\]
</dt> <dd>

Тип: **викпикселформатгуид \** _

Указатель, получающий GUID формата пикселей, в котором хранится битовая карта.

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



 

 




