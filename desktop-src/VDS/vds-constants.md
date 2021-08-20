---
description: Константы службы VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Константы службы VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9fa0c6196e1085de3a5433750b890e2ad3bc42f4a86022587f02157521eacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125697"
---
# <a name="vds-constants"></a>Константы службы VDS

\[начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API Windows служба хранилища управления](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Константы службы VDS классифицируются следующим образом:

-   [Константы состояния объекта](#object-status-constants)
-   [Константы для указания automagic](#automagic-hints-constants)
-   [Прочие константы](#miscellaneous-constants)

### <a name="object-status-constants"></a>Константы состояния объекта



| Константа           | Значение |
|--------------------|-------|
| СОСТОЯНИЕ \_ неизвестно    | 0     |
| СОСТОЯНИЕ в \_ сети     | 1     |
| СОСТОЯНИЕ \_ не \_ Готово | 2     |
| СОСТОЯНИЕ \_ без \_ носителя  | 3     |
| СОСТОЯНИЕ " \_ вне сети"    | 4     |
| СОСТОЯНИЕ " \_ Ошибка"     | 5     |
| \_отсутствует состояние    | 6     |



 

### <a name="automagic-hints-constants"></a>Константы для указания automagic



| Константа                               | Значение   |
|----------------------------------------|---------|
| \_мостлиреадс указание \_ VDS                 | 0x0002L |
| \_оптимизефорсекуентиалреадс указание \_ VDS  | 0x0004L |
| \_оптимизефорсекуентиалвритес указание \_ VDS | 0x0008L |
| \_ремапенаблед указание \_ VDS                | 0x0020L |
| \_вритесраугхкачинженаблед указание \_ VDS  | 0x0040L |
| \_хардваречекксуменаблед указание \_ VDS     | 0x0080L |
| \_исянкабле указание \_ VDS                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Прочие константы



| Константа                     | Значение      |
|------------------------------|------------|
| \_Минимальный приоритет повторного создания VDS \_ \_  | 0x0001L    |
| \_ \_ сведения о LUN VDS для ver \_   | 1          |
| Максимальная \_ \_ Длина ComputerName    | 15         |
| Максимальная \_ \_ Длина PROVIDERNAME    | 200        |
| Максимальная \_ \_ Длина VERSIONSTRING   | 16         |
| \_prop буква диска \_          | н/д        |
| МАКСИМАЛЬНЫЙ \_ \_ Размер имени \_ FS          | 8          |
| Недопустимый \_ \_ idx члена         | 0xFFFFFFFF |
| \_ \_ Длина имени раздела \_ GPT | 36         |
| МАКСИМАЛЬНЫЙ \_ путь                    | 260        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ссылка на службу VDS](vds-reference.md)
</dt> </dl>

 

 
