---
description: Проверяет, что профиль пользователя в сети загружен.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Функция Онпрофилелоадед (Лсаидпров. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 6a8ed0d96ab7c9c63f9574472cac0daedba54e42beec244271efcc309c04dd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921148"
---
# <a name="onprofileloaded-function"></a>Функция Онпрофилелоадед

Проверяет, что профиль пользователя в сети загружен.

## <a name="syntax"></a>Синтаксис


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Провидерхандле* \[ окне\]
</dt> <dd>

Обработчик поставщика.

</dd> <dt>

*UserToken* \[ окне\]
</dt> <dd>

Токен пользователя, профиль которого загружается или выгружается.

</dd> <dt>

*Загружено* \[ окне\]
</dt> <dd>

**Значение true** , если профиль загружен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает состояние \_ Success.

Если функция завершается с ошибкой, функция возвращает ненулевой код ошибки, который является специфической для поставщика ошибкой в целях диагностики.

## <a name="remarks"></a>Remarks

Эта функция вызывается каждый раз при вызове функции [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) . Он не синхронизирован с **LoadUserProfile**; Это значит, что **LoadUserProfile** мог вернуть, а профиль мог быть выгружен на момент вызова функции. Эта функция может вызываться несколько раз даже после загрузки профиля. Поставщик удостоверений не должен рассчитывать на то, что вызов этой функции с *загрузкой* , РАВНым true, должен сопровождаться вызовом с параметром *Loaded* , равным false.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Лсаидпров. h</dt> </dl> |



 

 
