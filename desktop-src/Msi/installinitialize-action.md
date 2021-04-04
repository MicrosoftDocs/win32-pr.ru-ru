---
description: Действие Инсталлинитиализе и функции InstallFinalize отмечают начало и конец последовательности действий, которые изменяют систему.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Действие Инсталлинитиализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810301"
---
# <a name="installinitialize-action"></a>Действие Инсталлинитиализе

Действие Инсталлинитиализе и [функции InstallFinalize](installfinalize-action.md) отмечают начало и конец последовательности действий, которые изменяют систему.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Инсталлинитиализе должно быть упорядочено до любых действий, изменяющих систему, таких как действие [инсталлфилес](installfiles-action.md) , действие [Вритерегистривалуес](writeregistryvalues-action.md) , действие [селфрегмодулес](selfregmodules-action.md) и действие [процесскомпонентс](processcomponents-action.md) . Следовательно, действие Инсталлинитиализе должно быть упорядочено до действия [функции InstallFinalize](installfinalize-action.md) и действия [инсталлексекуте](installexecute-action.md) .

[Настраиваемые действия](custom-actions.md) , изменяющие пакет установщик Windows, например добавление строк в таблицу, обрабатывающую устанавливаемые ресурсы, такие как таблица [реестра](registry-table.md) или таблица [дупликатефиле](duplicatefile-table.md) , должны быть упорядочены перед действием инсталлинитиализе.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

 

 



