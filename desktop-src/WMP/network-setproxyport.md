---
title: Метод Network. Сетпроксипорт
description: Метод Сетпроксипорт указывает используемый порт прокси-сервера. | Метод Network. Сетпроксипорт
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- Сетпроксипорт метод Windows Media Player
- Сетпроксипорт метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Сетпроксипорт
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694402"
---
# <a name="networksetproxyport-method"></a>Метод Network. Сетпроксипорт

Метод **сетпроксипорт** указывает используемый порт прокси-сервера.

## <a name="syntax"></a>Синтаксис


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*протокол* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> <dt>

*порт* \[ окне\]
</dt> <dd>

**Число** (**длинное**), определяющее используемый порт прокси-сервера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **сетпроксипорт** , чтобы указать номер порта прокси-сервера проигрывателя Windows Media для протокола MMS. Номер порта извлекается из HTML-элемента ввода с идентификатором ID = "PORT". Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
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

 

 





