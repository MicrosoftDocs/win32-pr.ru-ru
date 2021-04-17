---
title: Метод Network. setProxySettings
description: Метод setProxySettings указывает параметр прокси-сервера для данного протокола.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- setProxySettings метод Windows Media Player
- setProxySettings метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694657"
---
# <a name="networksetproxysettings-method"></a>Метод Network. setProxySettings

Метод **setProxySettings** указывает параметр прокси-сервера для данного протокола.

## <a name="syntax"></a>Синтаксис


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*протокол* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> <dt>

*параметр* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее одно из следующих значений.



| Значение | Описание                                                          |
|-------|----------------------------------------------------------------------|
| 0     | Не используйте прокси-сервер.                                           |
| 1     | Используйте параметры прокси-сервера текущего браузера (допустим только для HTTP). |
| 2     | Используйте заданные вручную параметры прокси-сервера.                           |
| 3     | Автоматическое определение параметров прокси-сервера.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере используется JScript с HTML-элементом SELECT, **который позволяет пользователю указать параметр прокси-сервера проигрывателя Windows Media для протокола HTTP. Объект Player** создан с идентификатором "Player".


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

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

 

 





