---
title: Имстскаксевентс Онремотепрограмдисплайед, метод
description: Вызывается при отображении программы RemoteApp.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотепрограмдисплайед
- Службы удаленных рабочих столов метода Онремотепрограмдисплайед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онремотепрограмдисплайед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802734"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a>Метод Имстскаксевентс:: Онремотепрограмдисплайед

Вызывается при отображении программы RemoteApp.

## <a name="syntax"></a>Синтаксис


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вбдисплайед* \[ окне\]
</dt> <dd>

Указывает, отображается ли приложение RemoteApp или скрыто.

</dd> <dt>

*удисплайинформатион* \[ окне\]
</dt> <dd>

Отображаемые сведения.

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**Шина \_ аппдисплай \_ аутореконнект**


</dt> <dd>

Выполняется автоматическое повторное подключение.

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**Шина \_ аппдисплай \_ десктофукед**


</dt> <dd>

Число RemoteApp было просто обнулено.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что приложение RemoteApp отображается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



 

 





