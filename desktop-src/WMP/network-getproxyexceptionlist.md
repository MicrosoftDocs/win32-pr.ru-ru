---
title: Метод Network. Жетпроксексцептионлист
description: Метод Жетпроксексцептионлист извлекает список исключений прокси-сервера.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- проигрыватель Windows Media метода жетпроксексцептионлист
- проигрыватель Windows Media метода жетпроксексцептионлист, класс сети
- класс проигрыватель Windows Media сети, метод жетпроксексцептионлист
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2becc6c74a5ada575f1bfa85473bd3204bf53a4a739640149cffdd57e3facf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054580"
---
# <a name="networkgetproxyexceptionlist-method"></a>Метод Network. Жетпроксексцептионлист

Метод **жетпроксексцептионлист** извлекает список исключений прокси-сервера.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = Network.getProxyExceptionList(
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

Этот метод возвращает **строку** , указывающую список узлов, разделенных точкой с запятой, для которых прокси-сервер пропускается. Возвращаемое значение имеет смысл только в том случае, если **жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).

## <a name="remarks"></a>Remarks

Это список компьютеров, доменов и (или) адресов, которые будут обходить прокси-сервер, если часть узла целевого URL-адреса совпадает с записью в списке.

\*Символ может использоваться в качестве подстановочного знака для списка записей. Например, \* . com будет соответствовать всем узлам в домене COM, а 67. \* будет соответствовать всем узлам в классе 67 подсети.

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **жетпроксексцептионлист** для вывода списка пропущенных прокси-серверов для протоколов MMS и HTTP. Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

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

 

 





