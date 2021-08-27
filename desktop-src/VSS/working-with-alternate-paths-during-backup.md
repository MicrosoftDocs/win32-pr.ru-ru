---
description: Существуют определенные обстоятельства, в которых файлы для резервного копирования не являются расположением по умолчанию для этих файлов.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Работа с альтернативными путями во время резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bc969c96d943b73a8a9d9609f004b4a0f738c46802af20a7dff22e34ebac56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124454"
---
# <a name="working-with-alternate-paths-during-backup"></a>Работа с альтернативными путями во время резервного копирования

Существуют определенные обстоятельства, в которых файлы для резервного копирования не являются расположением по умолчанию для этих файлов.

Например, некоторые модули записи не гарантируют, что данные записываются в течение временного интервала между событиями [*замораживания*](vssgloss-f.md) и [*разморозки*](vssgloss-t.md) . Такие модули записи могут создавать дублирующиеся файлы, содержащие последнюю известную удачную конфигурацию в исходном каталоге, отличном от используемого по умолчанию, или по [*альтернативному пути*](vssgloss-a.md).

Термин альтернативный путь, используемый с VSS, не следует путать с [*сопоставлением альтернативного расположения*](vssgloss-a.md). Альтернативные пути используются только во время операций резервного копирования и относятся к альтернативному источнику, из которого производится резервное копирование. Сопоставления альтернативного расположения используются только во время операций восстановления и ссылаются на альтернативное назначение для операций восстановления.

**Использование альтернативного пути во время резервного копирования**

1.  На этапе обнаружения операции резервного копирования (см. [Обзор этапа обнаружения резервных копий](overview-of-the-backup-discovery-phase.md)) инициатор запроса должен исследовать данные компонента каждого модуля записи с помощью [**ивссексаминевритерметадата::-Component**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) и Get Instances интерфейса [**ивссвмкомпонент**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .
2.  Затем инициатор запроса получает [*набор файлов*](vssgloss-f.md) , управляемых каждым компонентом, представленный экземплярами интерфейса [**ивссвмфиледеск**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) , вызывая метод [**ивссвмкомпонент::-File**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) .
3.  Помимо пути ([**ивссвмфиледеск::**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)ивссвмфиледеск), спецификации файла ([**:: жетфилеспек**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) и флага рекурсии ([**ивссвмфиледеск:: жетрекурсиве**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), объект [**ивссвмфиледеск**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) может содержать альтернативное расположение (используемое в качестве альтернативного пути для операций резервного копирования и сопоставление альтернативного расположения для операций восстановления) с помощью метода [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) .
4.  Если значение, возвращаемое [**ивссвмфиледеск:: жеталтернателокатион**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) , не равно null, приложения резервного копирования используют это значение вместо значения, полученного из [**Ивссвмфиледеск:: Multipath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) для выбора и поиска файлов для резервного копирования.
5.  Несмотря на использование альтернативного пути, запрашивающие стороны должны по-прежнему учитывать спецификацию файла и рекурсивные параметры, возвращаемые [**ивссвмфиледеск:: жетфилеспек**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) и [**Ивссвмфиледеск:: жетрекурсиве**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive).

Обратите внимание, что при восстановлении любой альтернативный путь, т. е. альтернативное расположение, возвращаемое экземпляром [**ивссвмфиледеск:: жеталтернателокатион**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) , получено из экземпляра [**ивссвмкомпонент**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), который, в свою очередь, был извлечен из экземпляра [**ивссексаминевритерметадата**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , получаемого путем извлечения хранимого документа метаданных модуля записи, не используется во время восстановления.

Либо путь по умолчанию (возвращаемый методом [**Multipath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) того же экземпляра [**ивссвмфиледеск**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) используется для определения расположения для восстановления, либо сопоставление альтернативного расположения, найденное с помощью метода [**ивссвмфиледеск:: жеталтернателокатион**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) , указывает, где следует восстановить файл (см. раздел [Работа с альтернативными расположениями во время восстановления](working-with-alternate-locations-during-restore.md)).

 

 



