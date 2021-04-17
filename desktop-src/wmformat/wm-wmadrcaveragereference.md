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
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700765"
---
# <a name="wmwmadrcaveragereference"></a>WM/Вмадркаверажереференце

Атрибут **WM/вмадркаверажереференце** содержит средний уровень громкости файла в кодировке.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмадркаверажереференце

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Комментарии

Проигрыватель Windows Media использует четыре атрибута для динамического управления диапазоном: **WM/вмадркаверажереференце**, **WM/вмадркпеакреференце**, **WM/вмадркаверажетаржет** и **WM/вмадркпеактаржет**. Все эти значения задаются модулем записи на основе информации из кодека при записи потоков с помощью кодека Windows Media Audio 9 или кодека Windows Media Audio 9 Professional. Для средних значений устанавливается средний уровень громкости потока, а для пиковых значений — максимальный уровень громкости в потоке. Ссылочные значения доступны только для чтения. Целевые значения задаются проигрывателем Windows Media при воспроизведении файла для записи параметров динамического управления диапазоном пользователя.

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

 

 




