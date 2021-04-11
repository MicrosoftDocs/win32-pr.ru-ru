---
description: Функция-посредник для метода "Colors".
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: Функция IWICPalette_GetColors_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265450"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>\_ \_ Функция прокси-сервера Ивикпалеттеных цветов

Функция-посредник для метода " [**Colors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) ".

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Указатель на этот объект [_ *ивикпалетте* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*колоркаунт* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер массива *пколорс* .

</dd> <dt>

*пколорс* \[ заполняет\]
</dt> <dd>

Тип: **викколор \** _

Указатель, получающий цвета палитры.

</dd> <dt>

_pcActualColors * \[ out\]
</dt> <dd>

Тип: **uint \** _

Фактический размер, необходимый для получения цветов палитры.

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



 

 




