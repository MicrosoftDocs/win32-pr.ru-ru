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
ms.openlocfilehash: ee8770029c8465d1e1a60349010847ff38fdac928bb61cd02b0e5a2b034538c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144009"
---
# <a name="configurableitemformat-property"></a>Конфигураблеитем. Format, свойство

Свойство **Format** объекта [**конфигураблеитем**](configurableitem-object.md) возвращает значение из столбца Format [таблицы модулеконфигуратион](moduleconfiguration-table.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Это свойство может иметь только следующие значения.



| Константа                        | Значение |
|---------------------------------|-------|
| **мсмконфигураблеитемтекст**     | 0     |
| **мсмконфигураблеитемкэй**      | 1     |
| **мсмконфигураблеитеминтежер**  | 2     |
| **мсмконфигураблеитембитфиелд** | 3     |



 

### <a name="c"></a>C++

См. раздел [**Получение функции \_ форматирования**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 2,0 или более поздней версии<br/>                                                    |
| Заголовок<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




