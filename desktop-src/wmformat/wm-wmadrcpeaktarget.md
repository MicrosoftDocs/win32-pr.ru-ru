---
title: WM/Вмадркпеактаржет
description: Атрибут WM/Вмадркпеактаржет содержит максимальный уровень громкости, запрошенный пользователем. это значение используется проигрыватель Windows Media для динамического управления диапазоном.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Формат Windows Media WM/Вмадркпеактаржет
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c87c8d62316bfa3e732d0cdc00e0fcb5295c30e675fd9c21fcd5ac766f239f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590684"
---
# <a name="wmwmadrcpeaktarget"></a>WM/Вмадркпеактаржет

Атрибут **WM/вмадркпеактаржет** содержит максимальный уровень громкости, запрошенный пользователем. это значение используется проигрыватель Windows Media для динамического управления диапазоном.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмадркпеактаржет

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Remarks

существует четыре атрибута, используемые проигрыватель Windows Media для динамического управления диапазоном: **WM/вмадркаверажереференце**, **wm/вмадркпеакреференце**, **wm/вмадркаверажетаржет** и **WM/вмадркпеактаржет**. все эти значения задаются модулем записи на основе информации из кодека при записи потоков с помощью кодека Windows media audio 9 или Windows Professional кодека media audio 9. Для средних значений устанавливается средний уровень громкости потока, а для пиковых значений — максимальный уровень громкости в потоке. Ссылочные значения доступны только для чтения. целевые значения задаются проигрыватель Windows Media при воспроизведении файла для записи параметров динамического управления диапазоном пользователя.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> <dt>

[**WM/Вмадркаверажереференце**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/Вмадркаверажетаржет**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/Вмадркпеакреференце**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




