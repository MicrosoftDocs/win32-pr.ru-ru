---
title: Player. URL
description: Свойство URL указывает или получает имя элемента мультимедиа для воспроизведения.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- проигрыватель Windows Media Player. URL
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00a6513350ee9c39855aba8168faf9ced788a0686a0fdbe845013dcc521142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572043"
---
# <a name="playerurl"></a>Player. URL

Свойство **URL** указывает или получает имя элемента мультимедиа для воспроизведения.

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **URL-адрес**

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи и не имеет значения по умолчанию.

## <a name="remarks"></a>Remarks

Этому свойству можно задать только URL-адрес в зоне безопасности с тем же или менее ограниченным, чем зона безопасности вызывающей программы или веб-страницы.

Приложения, которые открывают элементы мультимедиа из защищенного брандмауэра, будут иметь лучшую производительность, если адрес указан с помощью DNS-имени, а не IP-адреса.

Не вызывайте этот метод из кода обработчика событий. Вызов *проигрывателя*. **URL-адрес** из обработчика событий может привести к непредвиденным результатам.

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент ввода текста и элемент ввода HTML-кнопки. Элемент TEXT позволяет пользователю ввести путь для указания файла цифрового мультимедиа для воспроизведения. элемент BUTTON выполняет JScript, открывающий файл и запускающий проигрыватель Windows Media. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
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

 

 





