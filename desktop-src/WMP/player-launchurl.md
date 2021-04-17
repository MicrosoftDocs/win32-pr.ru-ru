---
title: Метод Player. Лаунчурл
description: Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру. | Метод Player. Лаунчурл
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Лаунчурл метод Windows Media Player
- метод Лаунчурл проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Лаунчурл
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685272"
---
# <a name="playerlaunchurl-method"></a>Метод Player. Лаунчурл

Метод **лаунчурл** отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру.

## <a name="syntax"></a>Синтаксис


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*URL-адрес* \[ окне\]
</dt> <dd>

**Строковое** значение, представляющее URL-адрес для запуска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод открывает только веб-страницы с использованием протоколов HTTP или HTTPS.

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере создается элемент кнопки HTML, который при нажатии отображает веб-сайт Майкрософт в новом окне браузера. Был создан элемент **Player** с идентификатором "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





