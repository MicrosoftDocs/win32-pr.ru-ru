---
title: вбрпеак
description: Атрибут Вбрпеак содержит максимальную скорость потока в закодированном потоке переменной скорости (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Формат Windows Media Вбрпеак
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9163e64aa3d309af8fd35626b7a4c0397ba4c949213ef351c1ac73ee9575a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704844"
---
# <a name="vbrpeak"></a>вбрпеак

Атрибут **вбрпеак** содержит максимальную скорость потока в закодированном потоке переменной скорости (VBR).

## <a name="global-constant"></a>Глобальная константа

g \_ всзвбрпеак

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Remarks

При доступе к интерфейсу **IWMHeaderInfo3** объекта Writer можно добавить или изменить это значение. В других объектах (редактор метаданных, читатель и синхронное средство чтения) это значение доступно только для чтения.

Модуль записи автоматически записывает значение **вбрпеак** для каждого потока VBR.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




