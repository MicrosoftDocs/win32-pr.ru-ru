---
description: ICE49 проверяет наличие записей реестра по умолчанию, которые не являются \_ типом reg SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911912"
---
# <a name="ice49"></a>ICE49

ICE49 проверяет наличие записей реестра по умолчанию, которые не являются типом **reg \_ SZ** .

## <a name="result"></a>Результат

ICE49 отправляет предупреждение, если имеется запись реестра по умолчанию, которая не является типом **reg \_ SZ** .

## <a name="example"></a>Пример

ICE49 сообщает следующее предупреждение для приведенного примера.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

Значение " \# 123" является значением реестра **DWORD** .

[Таблица реестра](registry-table.md) (частичная)



| Реестр | Имя | Значение |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Чтобы устранить это предупреждение, измените значение на введите **reg \_ SZ**.

Компоненты с **\_ SZами** , отличными от reg, являются допустимыми.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Синтаксис условных операторов](conditional-statement-syntax.md)
</dt> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



