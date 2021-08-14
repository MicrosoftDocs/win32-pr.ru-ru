---
description: Функция-посредник для метода Жетколоркаунт.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: Функция IWICPalette_GetColorCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 18d06760c696bb3e95dc638bea31d02228a108b9866e213013243ad4eeec441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206334"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a>Ивикпалетте \_ жетколоркаунт \_ -функция

Функция-посредник для метода [**жетколоркаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Указатель на этот объект [**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*пккаунт* \[ заполняет\]
</dt> <dd>

Тип: **uint \***

Указатель, получающий количество цветов в таблице цветов.

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



 

 




