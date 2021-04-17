---
title: Метод Network. Сетпроксибипассфорлокал
description: Метод Сетпроксибипассфорлокал задает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- Сетпроксибипассфорлокал метод Windows Media Player
- Сетпроксибипассфорлокал метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Сетпроксибипассфорлокал
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695080"
---
# <a name="networksetproxybypassforlocal-method"></a>Метод Network. Сетпроксибипассфорлокал

Метод **сетпроксибипассфорлокал** задает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.

## <a name="syntax"></a>Синтаксис


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*протокол* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> <dt>

*обход* \[ окне\]
</dt> <dd>

**Логическое значение** , указывающее, пропускается ли прокси-сервер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **сетпроксибипассфорлокал** , чтобы указать, пропускается ли прокси-сервер проигрывателя Windows Media при использовании протокола MMS, если сервер-источник находится в локальной сети. Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> </dl>

 

 





