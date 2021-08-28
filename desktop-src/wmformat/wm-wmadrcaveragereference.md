---
title: WM/Вмадркаверажереференце
description: Атрибут WM/Вмадркаверажереференце содержит средний уровень громкости файла в кодировке.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Формат Windows Media WM/Вмадркаверажереференце
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9948d71739aaee4f5f24f54701f8e335f8b7b79486c8820f7a5fdf48c068e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026952"
---
# <a name="wmwmadrcaveragereference"></a>WM/Вмадркаверажереференце

Атрибут **WM/вмадркаверажереференце** содержит средний уровень громкости файла в кодировке.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмадркаверажереференце

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Remarks

существует четыре атрибута, используемые проигрыватель Windows Media для динамического управления диапазоном: **WM/вмадркаверажереференце**, **wm/вмадркпеакреференце**, **wm/вмадркаверажетаржет** и **WM/вмадркпеактаржет**. все эти значения задаются модулем записи на основе информации из кодека при записи потоков с помощью кодека Windows media audio 9 или Windows Professional кодека media audio 9. Для средних значений устанавливается средний уровень громкости потока, а для пиковых значений — максимальный уровень громкости в потоке. Ссылочные значения доступны только для чтения. целевые значения задаются проигрыватель Windows Media при воспроизведении файла для записи параметров динамического управления диапазоном пользователя.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> <dt>

[**WM/Вмадркаверажетаржет**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/Вмадркпеакреференце**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/Вмадркпеактаржет**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




