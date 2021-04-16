---
description: Функция-посредник для метода GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: Функция IWICPalette_GetType_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712353"
---
# <a name="iwicpalette_gettype_proxy-function"></a>Ивикпалетте \_ \_ -функция GetType

Функция-посредник для метода [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Указатель на этот объект [_ *ивикпалетте* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*пепалеттетипе* \[ заполняет\]
</dt> <dd>

Тип: **[**викбитмаппалеттетипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _

Указатель, получающий тип палитры бимтап.

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



 

 




