---
description: Свойство Конфигураблеитемс только для чтения объекта Merge Возвращает коллекцию объектов Конфигураблеитем, каждый из которых представляет одну строку из таблицы Модулеконфигуратион.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configсвойство Ураблеитемс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 179594ba7fe7691edb9abe1f72d104742fe9bc9e3a4a23b728ad8607b94c444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013042"
---
# <a name="mergeconfigurableitems-property"></a>Merge.Config, свойство Ураблеитемс

Свойство **конфигураблеитемс** только для чтения объекта [**Merge**](merge-object.md) Возвращает коллекцию объектов [**конфигураблеитем**](configurableitem-object.md) , каждый из которых представляет одну строку из [таблицы модулеконфигуратион](moduleconfiguration-table.md). В семантическом виде каждый интерфейс в перечислителе представляет элемент, который может быть настроен потребителем модуля. Коллекция является коллекцией только для чтения и реализует стандартные интерфейсы коллекции только для чтения элементов (), Count () и \_ NewEnum (). Перечислитель **иенуммсмконфигитемс** реализует следующие (), Skip (), Reset () и Clone () со стандартной семантикой.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Значение свойства

## <a name="c"></a>C++

См. раздел [**Получение функции \_ конфигураблеитемс**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 2,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




