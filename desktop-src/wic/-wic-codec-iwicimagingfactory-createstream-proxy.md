---
description: Функция-посредник для метода Креатестреам.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: Функция IWICImagingFactory_CreateStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ec69a5cb9fe03fe6ebb1e9c31ac27fe2a81ab8df69ed5595c877ba5064e17953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088226"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a>IWICImagingFactory \_ креатестреам \_ -функция

Функция-посредник для метода [**креатестреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ппивикстреам* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***

Указатель, получающий указатель на новый [**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).

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



 

 




