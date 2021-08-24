---
title: оптималбитрате
description: Атрибут Оптималбитрате содержит битовую скорость, с которой файл лучше воспроизводить.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Формат Windows Media Оптималбитрате
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f670c2acd2f2190a5ee2bfd76994c219c6f967dbbd933520a8d4627236a0d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930634"
---
# <a name="optimalbitrate"></a>оптималбитрате

Атрибут **оптималбитрате** содержит битовую скорость, с которой файл лучше воспроизводить.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмоптималбитрате

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Remarks

Это закодированный атрибут.

Для файлов, содержащих потоки с переменной скоростью (VBR), это значение является пиковой скоростью потока в файле. Для файлов без VBR это значение совпадает с [**скоростью**](bit-rate.md).

Этот атрибут не может дублироваться на уровне файла. если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать свое нормальное значение объектам из пакета SDK Windows Media Format.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




