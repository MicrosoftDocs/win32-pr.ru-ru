---
title: Событие Player. Кдроммедиачанже
description: Событие Кдроммедиачанже возникает при вставке или извлечении компакт-диска или DVD-диска из дисковода CD или DVD. | Событие Player. Кдроммедиачанже
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Проигрыватель Windows Media Event Кдроммедиачанже
- Проигрыватель Windows Media Event Кдроммедиачанже, класс Player
- Класс проигрывателя Windows Media Player, событие Кдроммедиачанже
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
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704344"
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

## <a name="remarks"></a>Комментарии

Индекс дисковода компакт-дисков соответствует индексу объекта **CDROM** в **кдромколлектион**.

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект CDROM**](cdrom-object.md)
</dt> <dt>

[**Объект Кдромколлектион**](cdromcollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





