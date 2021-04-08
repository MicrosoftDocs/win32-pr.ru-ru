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
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069092"
---
# <a name="vbrpeak"></a>вбрпеак

Атрибут **вбрпеак** содержит максимальную скорость потока в закодированном потоке переменной скорости (VBR).

## <a name="global-constant"></a>Глобальная константа

g \_ всзвбрпеак

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Комментарии

При доступе к интерфейсу **IWMHeaderInfo3** объекта Writer можно добавить или изменить это значение. В других объектах (редактор метаданных, читатель и синхронное средство чтения) это значение доступно только для чтения.

Модуль записи автоматически записывает значение **вбрпеак** для каждого потока VBR.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




