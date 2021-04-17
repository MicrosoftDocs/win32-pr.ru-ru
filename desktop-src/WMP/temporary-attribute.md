---
title: Временный атрибут
description: Временный атрибут указывает, является ли список воспроизведения временным.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Временный атрибут Windows Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717829"
---
# <a name="temporary-attribute"></a>Временный атрибут

**Временный** атрибут указывает, является ли список воспроизведения временным.

**Замечания**

Если вы получили список воспроизведения из библиотеки, изменения, внесенные в список воспроизведения, будут отражены в библиотеке пользователя. Чтобы избежать этого, вызовите [ивмпплайлист:: сетитеминфо](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) , передав имя атрибута "Temporary" и значение "true". При этом экземпляр списка воспроизведения преобразуется во временный список воспроизведения, который можно изменить, не изменяя исходный список воспроизведения.

**Применимо к**:

-   [Списки воспроизведения](playlist-attributes-ref.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





