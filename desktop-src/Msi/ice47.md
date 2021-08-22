---
description: ICE47 проверяет таблицы функций и Феатурекомпонентс для функций с 1600 или более компонентами.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcf1f71af9bb8784c15b159836d329a94e7e6f33b34c31cbba72f9b31349a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381954"
---
# <a name="ice47"></a>ICE47

ICE47 проверяет таблицы [функций](feature-table.md) и [феатурекомпонентс](featurecomponents-table.md) для функций с 1600 или более компонентами.

## <a name="result"></a>Результат

ICE47 отправляет сообщение об ошибке, если компонент превышает максимальное ограничение в 1600 компонентов на компонент.

## <a name="example"></a>Пример

ICE47 сообщит о следующем предупреждении:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Таблица компонентов](feature-table.md) (частичная)



| Компонент  |
|----------|
| Feature1 |



 

[Таблица феатурекомпонентс](featurecomponents-table.md) (частичная)



| Действие   | Условие     |
|----------|---------------|
| Feature1 | Component1    |
| Feature1 | Component1600 |



 

Чтобы устранить это предупреждение, попробуйте разделить компонент на несколько функций.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



