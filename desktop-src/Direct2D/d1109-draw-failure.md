---
title: Сбой прорисовки D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Сбой вызова Draw объектом прорисовки
keywords:
- Сбой прорисовки D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b1d30d0b33cbeb053e37f9e52c3948009a19692dbe1c53eedab9dfd6623726a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814794"
---
# <a name="d1109-draw-failure"></a>D1109: сбой прорисовки

Вызов Draw невыполненным \[ *ресурсом* целевого объекта прорисовки \] . Теги \[ *TAG1*, *tag2* \] .

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*ресурсов*
</dt> <dd>

Адрес целевого объекта прорисовки.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*TAG1*
</dt> <dd>

Первое значение тега (Дополнительные сведения см. в [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Второе значение тега (Дополнительные сведения см. в [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Уровень ошибки | Предупреждение |



 

## <a name="possible-causes"></a>Возможные причины

Вызов рисования может завершиться неудачей по многим причинам. Дополнительные сведения см. в документации по пакету SDK для Direct2D для метода, который завершился ошибкой.

 

 