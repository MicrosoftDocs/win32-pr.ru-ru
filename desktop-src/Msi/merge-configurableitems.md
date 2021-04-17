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
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675361"
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



 

 




