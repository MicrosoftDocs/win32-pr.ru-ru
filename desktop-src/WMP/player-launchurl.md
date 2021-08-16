---
title: Метод Player. Лаунчурл
description: Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру. | Метод Player. Лаунчурл
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- проигрыватель Windows Media метода лаунчурл
- метод лаунчурл проигрыватель Windows Media, класс Player
- класс Player проигрыватель Windows Media, метод лаунчурл
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
ms.openlocfilehash: 79d22c65a29aaee9c849677dfa42acb5769bf30d2fb7079e305ee79632ef22e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134827"
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

## <a name="remarks"></a>Remarks

Этот метод открывает только веб-страницы с использованием протоколов HTTP или HTTPS.

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





