---
description: Свойство Format объекта Конфигураблеитем возвращает значение из столбца Format таблицы Модулеконфигуратион.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Свойство Конфигураблеитем. Format (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651897"
---
# <a name="configurableitemformat-property"></a>Конфигураблеитем. Format, свойство

Свойство **Format** объекта [**конфигураблеитем**](configurableitem-object.md) возвращает значение из столбца Format [таблицы модулеконфигуратион](moduleconfiguration-table.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Это свойство может иметь только следующие значения.



| Константа                        | Значение |
|---------------------------------|-------|
| **мсмконфигураблеитемтекст**     | 0     |
| **мсмконфигураблеитемкэй**      | 1     |
| **мсмконфигураблеитеминтежер**  | 2     |
| **мсмконфигураблеитембитфиелд** | 3     |



 

### <a name="c"></a>C++

См. раздел [**Получение функции \_ форматирования**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 2,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




