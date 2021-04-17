---
title: External. Аттемптлогин, метод
description: Метод Аттемптлогин отображает диалоговое окно, чтобы пользователь мог попытаться войти в Интернет-магазин.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Аттемптлогин метод Windows Media Player
- Аттемптлогин метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Аттемптлогин
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695065"
---
# <a name="externalattemptlogin-method"></a>External. Аттемптлогин, метод

Метод **аттемптлогин** отображает диалоговое окно, чтобы пользователь мог попытаться войти в Интернет-магазин.

## <a name="syntax"></a>Синтаксис


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если при входе в систему возникает изменение состояния входа, проигрыватель Windows Media вызывает событие [онлогинчанже](external-onloginchange-event.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Внешнее событие Онлогинчанже**](external-onloginchange-event.md)
</dt> <dt>

[**External. Усерлогжедин**](external-userloggedin.md)
</dt> <dt>

[**Ивмпконтентпартнер:: login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Управление именем входа**](managing-login.md)
</dt> </dl>

 

 





