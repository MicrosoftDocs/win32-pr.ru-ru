---
title: Событие Player. Аудиолангуажечанже
description: Событие Аудиолангуажечанже возникает при изменении текущего звукового языка. | Событие Player. Аудиолангуажечанже
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Проигрыватель Windows Media Event Аудиолангуажечанже
- Проигрыватель Windows Media Event Аудиолангуажечанже, класс Player
- Класс проигрывателя Windows Media Player, событие Аудиолангуажечанже
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704348"
---
# <a name="playeraudiolanguagechange-event"></a>Событие Player. Аудиолангуажечанже

Событие **аудиолангуажечанже** возникает при изменении текущего звукового языка.

## <a name="syntax"></a>Синтаксис


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Надежно* 
</dt> <dd>

**Число** (**длинное**), определяющее новый идентификатор локали (LCID).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.

Значение параметров события указывается проигрывателем Windows Media, и к нему можно получить доступ или передать методу в импортированном файле Microsoft JScript, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Controls. Куррентаудиолангуаже**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





