---
description: Действие Инсталлинитиализе и функции InstallFinalize отмечают начало и конец последовательности действий, которые изменяют систему.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Действие Инсталлинитиализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7031ab79bc099ea067fd8d83cb83d8cefd1f36a1e83f696a1ee3b4487b3cac88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996574"
---
# <a name="installinitialize-action"></a>Действие Инсталлинитиализе

Действие Инсталлинитиализе и [функции InstallFinalize](installfinalize-action.md) отмечают начало и конец последовательности действий, которые изменяют систему.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Инсталлинитиализе должно быть упорядочено до любых действий, изменяющих систему, таких как действие [инсталлфилес](installfiles-action.md) , действие [Вритерегистривалуес](writeregistryvalues-action.md) , действие [селфрегмодулес](selfregmodules-action.md) и действие [процесскомпонентс](processcomponents-action.md) . Следовательно, действие Инсталлинитиализе должно быть упорядочено до действия [функции InstallFinalize](installfinalize-action.md) и действия [инсталлексекуте](installexecute-action.md) .

[настраиваемые действия](custom-actions.md) , изменяющие пакет установщик Windows, например добавление строк в таблицу, обрабатывающую устанавливаемые ресурсы, такие как таблица [реестра](registry-table.md) или таблица [дупликатефиле](duplicatefile-table.md) , должны быть упорядочены перед действием инсталлинитиализе.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

 

 



