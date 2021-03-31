---
description: Функция-посредник для метода Хасалфа.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: Функция IWICPalette_HasAlpha_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998933"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a>Ивикпалетте \_ хасалфа \_ -функция

Функция-посредник для метода [**хасалфа**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Указатель на этот объект [_ *ивикпалетте* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*пфхасалфа* \[ заполняет\]
</dt> <dd>

Тип: **bool \** _

Указатель, который получает, `TRUE` Если палитра содержит прозрачный цвет. в противном случае — значение `FALSE` .

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



 

 




