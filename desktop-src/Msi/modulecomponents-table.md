---
description: Таблица Модулекомпонентс содержит список компонентов, найденных в модуле слияния.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Таблица Модулекомпонентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25216833022ada7592511091c6954222d8ebf354e732c95a54e8857948963541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926484"
---
# <a name="modulecomponents-table"></a>Таблица Модулекомпонентс

Таблица Модулекомпонентс содержит список компонентов, найденных в модуле слияния.

Таблица Модулекомпонентс содержит следующие столбцы.



| Столбец    | Type                         | Ключ | Допускает значения NULL |
|-----------|------------------------------|-----|----------|
| Компонент | [Идентификатор](identifier.md) | Д   | Нет        |
| ModuleID  | [Идентификатор](identifier.md) | Д   | Нет        |
| Язык  | [Integer](integer.md)       | Д   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>См
</dt> <dd>

Идентификатор, ссылающийся на компонент в модуле слияния. Столбец Component является внешним ключом к [таблице Component](component-table.md). Запись в столбце Component должна соответствовать соглашению об именовании при [именовании первичных ключей в базах данных модуля слияния](naming-primary-keys-in-merge-module-databases.md).

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Идентификатор модуля слияния. Это внешний ключ для [таблицы ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Языке
</dt> <dd>

Идентификатор языка описывает язык по умолчанию для модуля слияния. Идентификатор языка имеет десятичный формат, например, Английский (США) — 1033. Внешний ключ к [таблице ModuleSignature](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Преобразования языка должны иметь возможность обновлять эту таблицу, если модуль слияния поддерживает несколько языков.

 

 



