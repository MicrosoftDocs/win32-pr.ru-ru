---
description: Действие Мсипублишассемблиес управляет объявлением сборок среды CLR и сборок Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Действие Мсипублишассемблиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664543"
---
# <a name="msipublishassemblies-action"></a>Действие Мсипублишассемблиес

Действие Мсипублишассемблиес управляет объявлением сборок среды CLR и сборок Win32. Действие запрашивает [таблицу мсиассембли](msiassembly-table.md) , чтобы определить, какие сборки содержат компоненты, объявляемые или установленные в глобальном кэше сборок, а также какие сборки имеют родительский компонент, объявленный или установленный в расположении, изолированном для конкретного приложения. Дополнительные сведения см. в разделе [Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).

В операционных системах Microsoft Windows XP и более поздних версиях установщик Windows может устанавливать сборки Win32 как [Параллельные сборки](side-by-side-assemblies.md). Дополнительные сведения см. в разделе [о изолированных приложениях и параллельных сборках](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Мсипублишассемблиес должно следовать после [действия инсталлинитиализе](installinitialize-action.md) в таблице [Инсталлексекутесекуенце](installexecutesequence-table.md) или [таблице адвтексекутесекуенце](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия |
|-------|----------------------------|
| \[1\] | Контекст приложения.       |
| \[2\] | Имя сборки.             |



 

## <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе [сборки](assemblies.md).

[Действие мсиунпублишассемблиес](msiunpublishassemblies-action.md) управляет объявлением удаляемых сборок.

 

 
