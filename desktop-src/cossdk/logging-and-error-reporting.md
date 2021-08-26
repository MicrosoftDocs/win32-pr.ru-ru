---
description: Ведение журнала и отчеты об ошибках
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Ведение журнала и отчеты об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d974b4043b4365839aec6a4fae392ae1d84900e8b8347949147b8df13326bd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990764"
---
# <a name="logging-and-error-reporting"></a>Ведение журнала и отчеты об ошибках

## <a name="log-file"></a>Файл журнала

COMREPL создает файл журнала, содержащий состояние и сообщения об ошибках. Этот файл хранится на компьютере, где COMREPL был запущен в% системдир% \\ COM- \\ репликации \\ Comrepl. log.

Этот файл журнала удаляется при запуске фазы копирования. При последующей установке в целевые объекты будут добавлены к файлу.

## <a name="error-handling"></a>Обработка ошибок

Ошибки указаны в файле журнала, описанном выше. Подробные сведения об ошибках также можно найти в журнале событий на исходном или целевом компьютере.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление файлами](file-management.md)
</dt> <dt>

[Этапы репликации](replication-phases.md)
</dt> <dt>

[Использование COMREPL](using-comrepl.md)
</dt> <dt>

[Что реплицируется](what-gets-replicated.md)
</dt> </dl>

 

 



