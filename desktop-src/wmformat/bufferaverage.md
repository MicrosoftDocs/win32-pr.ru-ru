---
title: буфферавераже
description: Атрибут Буфферавераже содержит средний размер буфера, необходимый для потока с переменной скоростью (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- Формат Windows Media Буфферавераже
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd839bff96f5ba327e585f8608bd4612fc047d354c24fee972e507ea5ca681f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656124"
---
# <a name="bufferaverage"></a>буфферавераже

Атрибут **буфферавераже** содержит средний размер буфера, необходимый для потока с переменной СКОРОСТЬЮ (VBR).

## <a name="global-constant"></a>Глобальная константа

g \_ всзбуфферавераже

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Remarks

При доступе к интерфейсу **IWMHeaderInfo3** объекта Writer можно добавить или изменить это значение. В других объектах (редактор метаданных, читатель и синхронное средство чтения) это значение доступно только для чтения.

Модуль записи автоматически записывает значение **буфферавераже** для каждого потока VBR.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




