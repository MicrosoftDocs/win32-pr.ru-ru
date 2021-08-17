---
title: WM/GenreID
description: Атрибут WM/GenreID содержит идентификатор жанра, соответствующий содержимому тега ТКОН в ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Формат Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9355a16196d386d4ec3f2a98588eced2981f8e62a3df96a9c0d094551a10a733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930444"
---
# <a name="wmgenreid"></a>WM/GenreID

Атрибут **WM/GenreID** содержит идентификатор жанра, соответствующий содержимому тега Ткон в ID3v2. Он должен содержать идентификатор жанра в круглых скобках, при необходимости за которым следует уточнение, описывающее жанр. Дополнительные сведения см. в спецификации ID3v2.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмженреид

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Предпочтительным атрибутом для указания жанра является [**WM/жанр**](wm-genre.md). Используйте его в качестве предпочтения к этому атрибуту.

Если изменить файл **WM/жанр** или **WM/GENREID** в файле MP3, то другой атрибут будет изменен на Match.

### <a name="example"></a>Пример



| Тип файла | Пример значения   |
|-----------|-----------------|
| звук;     | "(4) еуродиско" |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




