---
description: Действие Мсиунпублишассемблиес управляет объявлением сборок среды CLR и удаляемых сборок Win32.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Действие Мсиунпублишассемблиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f640338e13f53b115ca3b93aa2a63987efb5aa7cf053d4c8a59d8d20d0f7e3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943901"
---
# <a name="msiunpublishassemblies-action"></a>Действие Мсиунпублишассемблиес

Действие Мсиунпублишассемблиес управляет объявлением сборок среды CLR и удаляемых сборок Win32. Действие запрашивает [таблицу мсиассембли](msiassembly-table.md) , чтобы определить, какие сборки были объявлены или установлены, удаляются из глобального кэша сборок и какие сборки содержат объявленный или установленный родительский компонент, который удаляется из расположения, изолированного для конкретного приложения. Дополнительные сведения см. в разделе [Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).

в системах под управлением Windows XP и более поздних версий установщик Windows может устанавливать сборки Win32 как [параллельные сборки](side-by-side-assemblies.md). Дополнительные сведения см. в разделе [о изолированных приложениях и параллельных сборках](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Мсиунпублишассемблиес должно следовать после [действия инсталлинитиализе](installinitialize-action.md) в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия |
|-------|----------------------------|
| \[1\] | Контекст приложения.       |
| \[2\] | Имя сборки.             |



 

## <a name="remarks"></a>Remarks

[Действие мсипублишассемблиес](msipublishassemblies-action.md) управляет объявлением объявляемых или установленных сборок.

 

 
