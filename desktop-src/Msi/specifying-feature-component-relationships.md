---
description: Каждая установщик Windowsная функция использует один или несколько установщик Windows компонентов, а компоненты могут совместно использовать компоненты.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Указание отношений Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673338"
---
# <a name="specifying-feature-component-relationships"></a>Указание отношений Feature-Component

Каждая [установщик Windowsная функция](windows-installer-features.md) использует один или несколько [установщик Windows компонентов](windows-installer-components.md), а компоненты могут совместно использовать компоненты. В [таблице феатурекомпонентс](featurecomponents-table.md) определяется связь между компонентами и компонентами. См. раздел [основные таблицы](core-tables-group.md) и [компоненты и](components-and-features.md) компоненты в обзоре установщик Windows. В этом разделе вы добавите сведения в таблицу Феатурекомпонентс образца Notepad.

Используйте редактор базы данных, чтобы открыть MNP2000.msi и ввести следующие данные в пустую таблицу Феатурекомпонентс.

[Таблица Феатурекомпонентс](featurecomponents-table.md)



| Функция\_ | Компонент\_ |
|-----------|-------------|
| Команды  | Команды    |
| Концерт   | Концерт     |
| Dance     | Dance       |
| Футбол  | Футбол    |
| Справка      | Справка        |
| Январь   | Январь     |
| невеарс  | невеарс    |
| Блокнот   | Блокнот     |
| Readme    | Блокнот     |



 

[Продолжить](adding-registry-information.md)

 

 



