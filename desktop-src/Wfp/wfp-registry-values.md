---
description: 'Значения реестра WFP находятся в следующем разделе реестра: HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Значения реестра WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664347"
---
# <a name="wfp-registry-values"></a>Значения реестра WFP

\[Значения реестра WFP не поддерживаются в Windows Vista.\]

WFP использует несколько значений реестра для настройки параметров. Значения реестра WFP находятся в следующем разделе реестра:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

Ниже приведены значения реестра WFP.

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**сфкдллкачедир**
</dt> <dd>

Расположение кэша. Это должен быть локальный путь. Значение по умолчанию —% SystemRoot% \\ system32 \\ Dllcache.

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

Параметры квоты. Этот параметр реестра может принимать одно из следующих значений.



| Значение                  | Значение                                                  |
|------------------------|----------------------------------------------------------|
| \_Квота SFC \_ все \_ файлы | Размер кэша DLL не ограничен. Это значение по умолчанию. |
| Другие значения           | Размер кэша DLL в файлах.                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**сфкскан**
</dt> <dd>

Параметры проверки. Этот параметр реестра может принимать одно из следующих значений.



| Значение             | Значение                                                   |
|-------------------|-----------------------------------------------------------|
| \_Проверка \_ обычного сканирования | Не проверять защищенные файлы при загрузке. Это значение по умолчанию. |
| \_сканирование SFC \_ всегда | Проверять защищенные файлы при каждой загрузке.                       |
| \_Проверка SFC \_   | Проверять защищенные файлы при следующей загрузке.                    |



 

</dd> </dl>

 

 



