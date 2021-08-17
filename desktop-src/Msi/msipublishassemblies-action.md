---
description: Действие Мсипублишассемблиес управляет объявлением сборок среды CLR и сборок Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Действие Мсипублишассемблиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524175a957249a48f7c72409ad7b4c55b31f642753db11875a9567ef35a2acf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804194"
---
# <a name="msipublishassemblies-action"></a>Действие Мсипублишассемблиес

Действие Мсипублишассемблиес управляет объявлением сборок среды CLR и сборок Win32. Действие запрашивает [таблицу мсиассембли](msiassembly-table.md) , чтобы определить, какие сборки содержат компоненты, объявляемые или установленные в глобальном кэше сборок, а также какие сборки имеют родительский компонент, объявленный или установленный в расположении, изолированном для конкретного приложения. Дополнительные сведения см. в разделе [Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).

в системах Microsoft Windows XP и более поздних версий установщик Windows может устанавливать сборки Win32 как [параллельные сборки](side-by-side-assemblies.md). Дополнительные сведения см. в разделе [о изолированных приложениях и параллельных сборках](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Мсипублишассемблиес должно следовать после [действия инсталлинитиализе](installinitialize-action.md) в таблице [Инсталлексекутесекуенце](installexecutesequence-table.md) или [таблице адвтексекутесекуенце](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия |
|-------|----------------------------|
| \[1\] | Контекст приложения.       |
| \[2\] | Имя сборки.             |



 

## <a name="remarks"></a>Remarks

Дополнительные сведения см. в разделе [сборки](assemblies.md).

[Действие мсиунпублишассемблиес](msiunpublishassemblies-action.md) управляет объявлением удаляемых сборок.

 

 
