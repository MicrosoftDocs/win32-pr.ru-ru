---
title: Метод Network. Жетпроксисеттингс
description: Метод Жетпроксисеттингс извлекает параметр прокси-сервера для данного протокола.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- проигрыватель Windows Media метода жетпроксисеттингс
- проигрыватель Windows Media метода жетпроксисеттингс, класс сети
- класс проигрыватель Windows Media сети, метод жетпроксисеттингс
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
ms.openlocfilehash: e142e7366c9e2b03e55dbd3768ee9c4fb41f30266d221a2ac5ac80019d5a7b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647444"
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



 

## <a name="remarks"></a>Remarks

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **жетпроксисеттингс** для вывода сообщения, которое предоставляет сведения о текущих параметрах прокси-сервера проигрывателя в окне браузера. Объект **Player** создан с идентификатором "Player".


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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> </dl>

 

 





