---
description: Функция-посредник для метода Инитиализекустом.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: Функция IWICPalette_InitializeCustom_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b68917782d768f526a21b16f22766c1a9add61eb5ee1987d27965b6f70a388db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088196"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a>Ивикпалетте \_ инитиализекустом \_ -функция

Функция-посредник для метода [**инитиализекустом**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Указатель на этот объект [**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*пколорс* \[ окне\]
</dt> <dd>

Тип: **викколор \***

Указатель на массив цветов.

</dd> <dt>

*колоркаунт* \[ окне\]
</dt> <dd>

Тип: **uint**

Число цветов в *пколорс*.

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



 

 




