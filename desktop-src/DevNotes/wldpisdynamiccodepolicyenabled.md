---
description: Извлекает значение, описывающее состояние принудительного применения политики Device Guard для динамического кода .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Функция Влдписдинамиккодеполициенаблед (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 12643bd542acac908c560a2094fb02e69d6d1aae62308e4ca4ece3be8bb85c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666365"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>Функция Влдписдинамиккодеполициенаблед

Извлекает значение, описывающее состояние принудительного применения политики Device Guard для динамического кода .NET.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*включено* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает **значение true** , если политика Device Guard обеспечивает применение политики динамического кода .NET. в противном случае возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.

## <a name="remarks"></a>Remarks

Динамический код относится к динамически созданному коду .NET CRL.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1803\]<br/>                           |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




