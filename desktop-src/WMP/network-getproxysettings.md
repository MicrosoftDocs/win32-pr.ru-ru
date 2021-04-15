---
title: Метод Network. Жетпроксисеттингс
description: Метод Жетпроксисеттингс извлекает параметр прокси-сервера для данного протокола.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- Жетпроксисеттингс метод Windows Media Player
- Жетпроксисеттингс метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Жетпроксисеттингс
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648759"
---
# <a name="networkgetproxysettings-method"></a>Метод Network. Жетпроксисеттингс

Метод **жетпроксисеттингс** извлекает параметр прокси-сервера для данного протокола.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Network.getProxySettings(
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

Этот метод возвращает **число** (**Long**), содержащее одно из следующих значений.



| Значение | Описание                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Прокси-сервер не используется.                                                |
| 1     | Используются параметры прокси-сервера для текущего браузера (допустимы только для HTTP). |
| 2     | Используются заданные вручную параметры прокси-сервера.                            |
| 3     | Параметры прокси-сервера обнаруживаются в автоматическом режиме.                                      |



 

## <a name="remarks"></a>Комментарии

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **жетпроксисеттингс** для вывода сообщения, которое предоставляет сведения о текущих параметрах прокси-сервера проигрывателя в окне браузера. Объект **Player** создан с идентификатором "Player".


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

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

 

 





