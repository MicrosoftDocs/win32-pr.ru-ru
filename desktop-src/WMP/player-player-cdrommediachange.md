---
title: Событие Player. Кдроммедиачанже
description: Событие Кдроммедиачанже возникает при вставке или извлечении компакт-диска или DVD-диска из дисковода CD или DVD. | Событие Player. Кдроммедиачанже
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- проигрыватель Windows Media событий кдроммедиачанже
- проигрыватель Windows Media событий кдроммедиачанже, класс Player
- класс проигрывателя проигрыватель Windows Media, событие кдроммедиачанже
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5e7301c1fb697f4dbbceea2d4dc46af1d884fe4b3e06166b5c24aa43502a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747390"
---
# <a name="playercdrommediachange-event"></a>Событие Player. Кдроммедиачанже

Событие **кдроммедиачанже** возникает при вставке или ИЗВЛЕЧЕНии компакт-диска или DVD-диска из дисковода CD или DVD.

## <a name="syntax"></a>Синтаксис


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кдромнум* 
</dt> <dd>

**Число** (**длинное**), указывающее индекс компакт-диска или DVD-дисковода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Индекс дисковода компакт-дисков соответствует индексу объекта **CDROM** в **кдромколлектион**.

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект CDROM**](cdrom-object.md)
</dt> <dt>

[**Объект Кдромколлектион**](cdromcollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





