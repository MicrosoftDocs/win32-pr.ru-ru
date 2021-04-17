---
description: Вызывается из любого шейдера нажатия, чтобы отклонить попадание и завершить шейдер.
ms.assetid: ''
title: Функция IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692032"
---
# <a name="ignorehit-function"></a>Функция IgnoreHit

Вызывается из [любого шейдера нажатия](any-hit-shader.md) , чтобы отклонить попадание и завершить шейдер. Поиск курсоров продолжится без фиксации расстояния и атрибутов для текущего попадания.  Вызов [**репорсит**](reporthit-function.md) в [шейдере пересечения](intersection-shader.md), если таковой имеется, возвратит значение false.  Все изменения, внесенные в полезные данные лучей вплоть до этой точки в шейдере, сохраняются.

## <a name="syntax"></a>Синтаксис

```
void IgnoreHit();

```


## <a name="return-value"></a>Возвращаемое значение

**void**

## <a name="remarks"></a>Комментарии

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер любых попаданий**](any-hit-shader.md)




## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




