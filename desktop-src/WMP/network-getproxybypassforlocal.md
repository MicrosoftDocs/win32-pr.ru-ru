---
title: Метод Network. Жетпроксибипассфорлокал
description: Метод Жетпроксибипассфорлокал извлекает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- проигрыватель Windows Media метода жетпроксибипассфорлокал
- проигрыватель Windows Media метода жетпроксибипассфорлокал, класс сети
- класс проигрыватель Windows Media сети, метод жетпроксибипассфорлокал
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
ms.openlocfilehash: 51f22eb6187938318d95b9dd7a473b58e216315210d4af41c29b352b2654cbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054562"
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

## <a name="remarks"></a>Remarks

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **жетпроксибипассфорлокал** , чтобы показать, настроен ли проигрыватель Windows Media для обхода прокси-сервера для локальных адресов. Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> <dt>

[**Network. Жетпроксисеттингс**](network-getproxysettings.md)
</dt> </dl>

 

 





