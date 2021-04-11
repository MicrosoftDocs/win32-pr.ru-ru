---
description: При установке сборки в изолированное расположение для конкретного приложения оно должно быть указано в \_ столбце Application File таблицы мсиассембли.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Установка и удаление сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272803"
---
# <a name="installing-and-removing-assemblies"></a>Установка и удаление сборок

При установке сборки в изолированное расположение для конкретного приложения оно должно быть указано в \_ столбце Application file [таблицы мсиассембли](msiassembly-table.md). Это поле является ключом в [таблице File](file-table.md). Установщик использует структуру каталогов, указанную в [таблице Directory](directory-table.md) , для установки сборки в тот же каталог, что и компонент, содержащий этот файл.

При установке сборки в глобальный кэш сборок значение в \_ столбце Application file [таблицы мсиассембли](msiassembly-table.md) должно быть равно null.

В следующих разделах описывается установка Win32 и сборок среды CLR.

-   [Установка сборок Win32](installation-of-win32-assemblies.md)
-   [Установка сборок среды CLR](installation-of-common-language-runtime-assemblies.md)

 

 



