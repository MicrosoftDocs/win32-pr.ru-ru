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
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140887"
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

## <a name="remarks"></a>Комментарии

Динамический код относится к динамически созданному коду .NET CRL.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




