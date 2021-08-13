---
description: Документ компонентов резервного копирования сохраняется экземплярами интерфейса Ивссбаккупкомпонентс.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Содержимое документа компонентов резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c844f2e9e106817c8201822d000c2f6cb94c0fa272bb5b165d98e4cc48b1c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248344"
---
# <a name="backup-components-document-contents"></a>Содержимое документа компонентов резервного копирования

Документ компонентов резервного копирования сохраняется экземплярами интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Этот интерфейс также содержит множество методов управления операциями резервного копирования, управления теневыми копиями и выполнения запросов к состоянию системы. Однако не все данные документа доступны напрямую через этот интерфейс.

Документ компонентов резервного копирования состоит из нескольких наборов данных.

-   Сведения о том, какие компоненты были явно добавлены в операцию резервного копирования или восстановления
-   Представление хранимой информации о компоненте и модуле записи
-   Сведения о состоянии операции резервного копирования и восстановления

Хотя сведения о компоненте доступны как для запрашивающего, так и для модуля записи, доступ к сведениям о состоянии предоставляется только модулю записи.

## <a name="component-inclusion-information"></a>Сведения об включении компонентов

Документ компоненты резервного копирования содержит список компонентов, явно включаемых в резервное копирование и восстановление инициатором запроса. Список содержит следующие сведения:

-   Явно включаемые [*выбираемые компоненты*](vssgloss-s.md).

    Включение этих файлов в операции резервного копирования обозначается [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) и в операциях восстановления с помощью [**Ивссбаккупкомпонентс:: сетселектедфорресторе**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Невыбираемые для резервного копирования подкомпоненты без выбора для предка компонента резервного копирования.

    Все эти компоненты должны быть включены, если в операцию включаются какие бы то ни было компоненты модуля записи. Включение этих файлов в операции резервного копирования обозначается [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) и в операциях восстановления с помощью [**Ивссбаккупкомпонентс:: сетселектедфорресторе**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Компоненты неявно добавляются в резервную копию ([*подкомпоненты*](vssgloss-s.md)), которые можно [*выбрать для восстановления*](vssgloss-s.md) и явно добавлять в восстановление.

    Эти компоненты могут быть либо выбираемыми, либо невыбираемыми, но иметь возможность выбора предка, который использовался для их неявного выбора для резервного копирования. Они добавляются в документ компонентов резервного копирования с помощью [**ивссбаккупкомпонентс:: аддресторесубкомпонент**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Удостоверения компонентов, неявно включаемых в восстановление, не хранятся в документе компоненты резервного копирования.

Служба VSS имеет доступ к сведениям о включении компонентов: модули записи без компонентов, явно включенные в восстановление или резервное копирование, не получают события VSS после создания [*PrepareForBackup*](vssgloss-p.md) или предварительно [*восстановленных*](vssgloss-p.md) событий.

Модули записи не могут напрямую запрашивать эти сведения. Это не является существенным ограничением, так как при проектировании отдельные модули записи VSS не должны требовать подробных сведений о состоянии других модулей записи в системе и, как отмечалось выше, они не будут участвовать в операции VSS.

Инициатор запроса может определить, какие компоненты были явно добавлены в операцию.

Метод [**ивссбаккупкомпонентс:: жетвритеркомпонентскаунт**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) возвращает число модулей записи со сведениями о компонентах, хранящихся в документе резервных копий (а не число компонентов в документе).

Инициатор запроса индексирует данные хранимой записи с помощью [**ивссбаккупкомпонентс:: жетвритеркомпонентс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), которая возвращает экземпляры интерфейса [**ивссвритеркомпонентсекст**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) . Интерфейс **ивссвритеркомпонентсекст** позволяет инициатору запроса получить [*класс модуля записи*](vssgloss-w.md) и [*экземпляр модуля*](vssgloss-w.md) записи участвующих модулей записи, а также получить доступ к сведениям о его компонентах, хранящихся в документе архивных компонентов.

## <a name="information-on-included-components"></a>Сведения о включенных компонентах

В документе компонентов резервного копирования содержится представление данных компонента (которые не включают сведения о пути и спецификации файла), доступ к которым осуществляется через экземпляры интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Запрашивающие стороны и модули записи получают доступ к экземплярам интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) различными способами.

Инициатор запроса проверяет данные компонента в модуле записи с помощью экземпляров интерфейса [**ивссвритеркомпонентсекст**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) , возвращаемого [**Ивссбаккупкомпонентс:: жетвритеркомпонентс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Помимо идентификационной информации модуля записи, интерфейс [**ивссвритеркомпонентсекст**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) предоставляет массив экземпляров интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) — по одному для каждого из выбранных модулей записи.

Как отмечалось в [жизненном цикле документа компоненты резервного копирования](backup-components-document-life-cycle.md), модули записи могут получить доступ к одной и той же информации через интерфейс [**ивссвритеркомпонентс**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) при обработке события PrepareForBackup, Препарефорснапшот, моментального снимка, баккупкомплете, с помощью инструкции RESTORE или на этапе восстановления.

[**Ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) позволяет модулю записи и инициатору запроса получить следующие сведения:

-   Имя, тип и [*логический путь*](vssgloss-l.md) компонента ([**жеткомпонентнаме**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**жеткомпоненттипе**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**жетлогикалпас**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Как компонент должен быть восстановлен, как указано в [*целевом объекте восстановления*](vssgloss-r.md) ([**Ивсскомпонент:: жетресторетаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Если при восстановлении файла использовалось альтернативное расположение ([**жеталтернателокатионмаппинг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**жеталтернателокатионмаппингкаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Новые целевые сведения (если таковые имеются) ([**жетневтаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**жетневтаржеткаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Сообщения об ошибках до и после восстановления ([**жетпрересторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**жетпостресторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Если для компонента [*резервного копирования*](vssgloss-s.md) , определяющего набор компонентов, выбран параметр для восстановления ([**исселектедфорресторе**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore)), то
-   Успешность резервного копирования или восстановления ([**жетбаккупсукцеедед**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**жетфилересторестатус**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Любые параметры резервного копирования или восстановления, которые могут быть заданы [**ивссбаккупкомпонентс:: сетбаккупоптионс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) или [**Ивссбаккупкомпонентс:: сетрестореоптионс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**жетбаккупоптионс**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)).
-   Метаданные для резервного копирования или восстановления метаданных конкретного модуля записи ([**жетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**жетрестореметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Сведения о временной метке ([**жетбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**жетпревиаусбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Сведения о подкомпонентах резервного копирования, явно включаемых в восстановление ([**жетресторесубкомпонент**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**жетресторесубкомпоненткаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

В отличие от запрашивающих, модули записи могут изменять определенную информацию в документе компоненты резервного копирования через интерфейс [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) :

-   Как компонент должен быть восстановлен, как указано в целевом объекте восстановления ([**ивсскомпонент:: сетресторетаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Метаданные для записи резервных копий и восстановления ([**ивсскомпонент:: сетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**Ивсскомпонент:: сетрестореметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)).
-   Сведения о временной метке ([**сетбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Сообщения об ошибках до и после восстановления ([**сетпрересторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**сетпостресторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Сведения о состоянии инициатора запроса

Запрашивающие стороны вставляют сведения о состоянии операции резервного копирования или восстановления в документ компонентов резервного копирования с помощью интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Приложения для записи могут запрашивать эти сведения с помощью класса [**квссвритер**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) .

Сведения о состоянии, хранящиеся в документе резервного копирования компонентов, включают следующее:

Общие сведения о резервной копии

-   Общий тип резервного копирования (добавочный, разностный или полный);<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетбаккупстате**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Извлекается модулями записи с помощью [ **квссвритер:: жетбаккуптипе**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетбаккупстате**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Извлекается модулями записи с помощью [ **квссвритер:: арекомпонентсселектед**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетбаккупстате**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Извлекается модулями записи с помощью [ **квссвритер:: исбутаблестатебаккедуп**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетбаккупстате**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Извлекается модулями записи с помощью [ **квссвритер:: испартиалфилесуппортенаблед**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Общие сведения о восстановлении

-   Общий тип восстановления (для восстановления — копирование или импорт)<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетресторестате**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Извлекается модулями записи с помощью [ **квссвритер:: жетресторетипе**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Сведения о вспомогательных файлах

-   Расположение файлов Ranges, используемых конкретным компонентом в частичных операциях с файлами<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетранжесфилепас**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Извлекается модулями записи (или запрашивающими стороны) с помощью [ **ивсскомпонент:: жетпартиалфиле**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Состояние информации

-   Укажите, успешно ли создана резервная копия одного из компонентов данного модуля записи<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетбаккупсукцеедед**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Извлекается модулями записи и запрашивающими стороны с помощью [ **ивсскомпонент:: жетбаккупсукцеедед**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Задается инициаторами запроса с помощью [ **ивссбаккупкомпонентс:: сетфилересторестатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Извлекается модулями записи и инициатором запроса с помощью [ **ивсскомпонент:: жетфилересторестатус**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Сведения о Writer-Settable

-   Дополнительная спецификация резервного копирования для одного из компонентов конкретного модуля записи<dl> <dt>

Задается модулями записи с помощью [ **ивсскомпонент:: сетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Извлекается модулями записи и запрашивающими стороны с помощью [ **ивсскомпонент:: жетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Задается модулями записи с помощью [ **ивсскомпонент:: сетрестореметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Извлекается модулями записи и запрашивающими стороны с помощью [ **ивсскомпонент:: жетрестореметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Задается модулями записи с помощью [ **ивсскомпонент:: сетбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Извлекается модулями записи и запрашивающими стороны с помощью [ **ивсскомпонент:: жетбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">Ивсскомпонент:: Сетбаккупстамп</a><dl> <dt>

Сохраняются и задаются запрашивающими стороны для определенного компонента с помощью [ **ивссбаккупкомпонентс:: сетпревиаусбаккупстамп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Извлекается модулями записи и запрашивающими стороны с помощью [ **ивсскомпонент:: жетпревиаусбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Задается модулями записи с помощью [**ивсскомпонент:: сетпрересторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) или [**Ивсскомпонент:: сетпостресторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Извлекается модулями записи и запрашивающими стороны с помощью [**ивсскомпонент:: жетпрересторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) или [**Ивсскомпонент:: жетпостресторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
