---
title: Устаревшая ссылка на восстановление системы
description: В этой документации описываются сведения о реализации репозитория, используемого устаревшей версией восстановления системы. Он не применяется к реализации восстановления системы в Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887695"
---
# <a name="legacy-system-restore-reference"></a>Устаревшая ссылка на восстановление системы

\[Эти сведения относятся только к Windows XP с пакетом обновления 2 (SP2).\]

В этой документации описываются сведения о реализации репозитория, используемого устаревшей версией восстановления системы. Он не применяется к реализации восстановления системы в Windows Vista.

## <a name="system-restore-repository-structure"></a>Структура репозитория восстановления системы

Windows XP с пакетом обновления 2 (SP2) содержит репозиторий для восстановления системы в следующей папке:% SYSTEMDRIVE% \\ сведения о системном томе. Этот репозиторий содержит сведения для точек восстановления, которые по сути являются моментальным снимком системы в данный момент времени.

Репозиторий структурирован следующим образом:

Восстановление **сведений о системных томах**    ** \_ {*GUID*}**       **Rp1**       **RP2**       **RP *n*-1**       **RP * n** *     ** \_ RESTORE {*GUID*}**       **Rp1**       **RP2**       **RP *n*-1**       **RP * n***

Чтобы определить \_ , какую папку Restore {*GUID*} использовать, прочитайте **идентификатор GUID** , указанный в следующем файле: SYSTEMROOT% \\ system32 \\ RESTORE \\MachineGUID.txt.

В каждой \_ папке Restore {*GUID*} \_ файл driver. cfg содержит сведения из структуры **\_ постоянной \_ конфигурации SR** , определенные следующим образом.

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a>Файлы, содержащиеся в каждой папке RP *n*

Каждая папка RP *n* содержит папку моментальных снимков, которая содержит следующее:

-   Моментальный снимок кустов реестра
-   Папка репозитория, содержащая моментальный снимок репозитория WMI.
-   Моментальный снимок базы данных COM+
-   Моментальный снимок базы данных IIS

Каждая папка RP *n* содержит файл RP. log, содержащий общие сведения о точке восстановления из структуры [**ресторепоинтинфов**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .

Каждая папка RP *n* может содержать файлы, используемые для наблюдения за изменениями точки восстановления. Первый файл называется Change. log, следующий файл называется Changed. log. 1 и т. д. Каждый файл журнала изменений содержит следующие структуры:

-   [**\_заголовок журнала \_ изменений**](change-log-header.md)
-   [**Изменить \_ \_Запись журнала**](change-log-entry.md)1
-   [**Изменить \_ \_Запись журнала**](change-log-entry.md)2
-   ...
-   [**Изменить \_ \_Запись журнала**](change-log-entry.md)*n*

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устаревшие структуры восстановления системы](legacy-system-restore-structures.md)
</dt> </dl>

 

 




