---
title: Метод Network. Жетпроксибипассфорлокал
description: Метод Жетпроксибипассфорлокал извлекает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- Жетпроксибипассфорлокал метод Windows Media Player
- Жетпроксибипассфорлокал метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Жетпроксибипассфорлокал
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704387"
---
# <a name="networkgetproxybypassforlocal-method"></a>Метод Network. Жетпроксибипассфорлокал

Метод **жетпроксибипассфорлокал** извлекает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.

## <a name="syntax"></a>Синтаксис


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*протокол* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **логическое значение** , указывающее, пропускается ли прокси-сервер. Возвращаемое значение имеет смысл только в том случае, если **жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).

## <a name="remarks"></a>Комментарии

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **жетпроксибипассфорлокал** , чтобы отобразить, настроен ли проигрыватель Windows Media на обход прокси-сервера для локальных адресов. Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> <dt>

[**Network. Жетпроксисеттингс**](network-getproxysettings.md)
</dt> </dl>

 

 





