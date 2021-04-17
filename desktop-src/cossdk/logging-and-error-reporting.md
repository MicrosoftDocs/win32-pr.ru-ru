---
description: Ведение журнала и отчеты об ошибках
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Ведение журнала и отчеты об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673143"
---
# <a name="logging-and-error-reporting"></a>Ведение журнала и отчеты об ошибках

## <a name="log-file"></a>Файл журнала

COMREPL создает файл журнала, содержащий состояние и сообщения об ошибках. Этот файл хранится на компьютере, где COMREPL был запущен в% системдир% \\ COM- \\ репликации \\ Comrepl. log.

Этот файл журнала удаляется при запуске фазы копирования. При последующей установке в целевые объекты будут добавлены к файлу.

## <a name="error-handling"></a>Обработка ошибок

Ошибки указаны в файле журнала, описанном выше. Подробные сведения об ошибках также можно найти в журнале событий на исходном или целевом компьютере.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление файлами](file-management.md)
</dt> <dt>

[Этапы репликации](replication-phases.md)
</dt> <dt>

[Использование COMREPL](using-comrepl.md)
</dt> <dt>

[Что реплицируется](what-gets-replicated.md)
</dt> </dl>

 

 



