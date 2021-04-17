---
title: Событие Player. Маркерхит
description: Событие Маркерхит возникает при достижении маркера. | Событие Player. Маркерхит
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Проигрыватель Windows Media Event Маркерхит
- Проигрыватель Windows Media Event Маркерхит, класс Player
- Класс проигрывателя Windows Media Player, событие Маркерхит
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685300"
---
# <a name="playermarkerhit-event"></a>Событие Player. Маркерхит

Событие **маркерхит** возникает при достижении маркера.

## <a name="syntax"></a>Синтаксис


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*маркернум* 
</dt> <dd>

**Число** (**длинное**), указывающее число попаданий маркера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





