---
description: Для работы с неявными выбранными компонентами требуется доступ к документам с метаданными и документами метаданных для модуля резервного копирования.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Выбор и работа со свойствами компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d06683bafb02802d84f152f1ceb662eb7491f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156103"
---
# <a name="selectability-and-working-with-component-properties"></a>Выбор и работа со свойствами компонентов

Для работы с неявными выбранными компонентами требуется доступ к документам с метаданными и документами метаданных для модуля резервного копирования.

Для этого имеются две причины:

-   Данные компонента, хранящиеся в документе резервных копий (представленном интерфейсом [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ), не имеют доступа к сведениям о наборе файлов компонентов — спецификации файла, пути и флаге рекурсии. (См. раздел [Работа с компонентом Backup Components](working-with-the-backup-components-document.md).)
-   Только компоненты, которые [*явно включены*](vssgloss-e.md) в документ резервных копий во время резервного копирования, содержат сведения, непосредственно хранящиеся в документе резервные компоненты. Запрашивающие стороны и модули записи должны использовать информацию, доступную через интерфейс [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , в сочетании с метаданными о [*логическом пути*](vssgloss-l.md) и документах метаданных модуля записи для получения сведений о и задании свойств [*неявно включаемых*](vssgloss-i.md) компонентов.

Вариант "Мивритер", обсуждаемый в разделе " [логические пути к компонентам](logical-pathing-of-components.md) ", можно использовать для демонстрации выбора для резервного копирования.



| Имя компонента | Логический путь            | Выбор для резервного копирования | Выбор для восстановления | Явно включена |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| Исполняемые файлы  | ""                      | Нет                     | Нет                      | Да                   |
| "Конфигфилес"  | Исполняемые файлы           | Нет                     | Нет                      | Да                   |
| "Лиценсеинфо"  | ""                      | Да                     | Нет                      | Да                   |
| Security     | ""                      | Да                     | Нет                      | Да                   |
| UserInfo     | Security              | Нет                     | Нет                      | Нет                   |
| Сертификаты | Security              | Нет                     | Нет                      | Нет                   |
| "Вритердата"   | ""                      | Да                     | Да                      | Да                   |
| Set1         | "Вритердата"            | Нет                     | Да                      | Нет                   |
| Янв          | "Вритердата \\ Set1"      | Нет                     | Нет                      | Нет                   |
| Уменьшение          | "Вритердата \\ Set1"      | Нет                     | Нет                      | Нет                   |
| Set2         | "Вритердата"            | Нет                     | Да                      | Нет                   |
| Янв          | "Вритердата \\ Set2"      | Нет                     | Нет                      | Нет                   |
| Уменьшение          | "Вритердата \\ Set2"      | Нет                     | Нет                      | Нет                   |
| Выбор        | "Вритердата \\ куерилогс" | Нет                     | Нет                      | Нет                   |
| Загрузка        | "Вритердата"            | Да                     | Да                      | Нет                   |
| Янв          | " \\ Использование вритердата"     | Нет                     | Нет                      | Нет                   |
| Уменьшение          | " \\ Использование вритердата"     | Нет                     | Нет                      | Нет                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Неявно включаемые компоненты в резервном наборе данных

При проверке документа метаданных модуля записи (см. [**ивссбаккупкомпонентс:: жетвритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) во время резервного копирования инициатор запроса должен хранить список всех компонентов, их [*логические пути*](vssgloss-l.md)и сведения о наборах файлов.

Чтобы определить список файлов для любого (явно или неявно) включенного компонента, необходимы сведения о наборе файлов и исключенном файле.

Для невыбираемых компонентов резервного копирования без возможности выбора для предков резервного копирования и выбора для компонентов резервного копирования, которые не определяют [*набор компонентов*](vssgloss-c.md), для определения всех кандидатов компонента резервного копирования необходимы только сведения о наборе файлов и исключенных файлах, так как эти компоненты не определяют подкомпоненты.

Для явно включаемых компонентов для резервного копирования, определяющих набор компонентов, файл устанавливает и исключает сведения о файле как для определяющего компонента, так и во всех [*подкомпонентах*](vssgloss-s.md) для выбора файлов для резервного копирования.

Это означает, что резервные наборы данных для компонентов "Executable", "Конфигфилес" и "Лиценсеинфо" можно найти только путем проверки метаданных модуля записи для этих компонентов с помощью экземпляров интерфейса [**ивссвмкомпонент**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .

Однако если Вритердата явно включено в резервную копию, необходимо изучить его экземпляр интерфейса [**ивссвмкомпонент**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) и для "set1", "Jan" (с логическим путем "вритердата \\ Set1"), "Dec" (с логическим путем "вритердата \\ Set1"), "set2", "Jan" (с логическим путем "вритердата \\ Set2"), "Dec" (с логическим путем "вритердата \\ Set2"), "Query", "Usage", "Янв" (с логическим путем "Вритердата \\ Usage") и "Dec" (с логическим путем "writerData \\ Usage").

Для этого инициатору запроса необходимо сначала указать, что компонент "Вритердата" (логический путь "") доступен для выбора. Затем он должен проверять все другие компоненты, управляемые модулем записи, чтобы определить, является ли первый элемент в их логическом пути "Вритердата". Эти компоненты, имеющие "Вритердата" в качестве ведущих членов их логического пути, определяются как подкомпоненты "Вритердата" и неявно выбираются при явном выборе.

На самом деле необходимо выполнить аналогичную проверку, чтобы определить, что ни один из компонентов не имеет "Лиценсеинфо" в качестве ведущего члена его логического пути, и, таким образом, "Лиценсеинфо" не имеет подкомпонентов.

Из-за сложности этого механизма в VSS многие модули записи инициаторов могут оказаться полезными при создании собственных структур для хранения компонентов и сведений о резервных наборах как для явно, так и для неявно добавляемых компонентов.

## <a name="properties-of-implicitly-included-components"></a>Свойства неявно включаемых компонентов

Во время операций восстановления и резервного копирования экземпляры интерфейсов [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) и [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) используются как для получения сведений о компонентах, так и для установки или изменения свойств компонента. Однако только явно включаемые компоненты будут иметь экземпляры интерфейса **ивсскомпонент** или будут доступны интерфейсу **ивссбаккупкомпонентс** .

Некоторые свойства задаются на уровне компонентов в области. К этим свойствам относятся следующие.

-   Состояние резервного копирования и восстановления: <dl>

[**Ивссбаккупкомпонентс:: Сетбаккупсукцеедед**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**Ивсскомпонент:: Жетбаккупсукцеедед**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**Ивссбаккупкомпонентс:: Сетфилересторестатус**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**Ивсскомпонент:: Жетфилересторестатус**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Параметры резервного копирования и восстановления: <dl>

[**Ивссбаккупкомпонентс:: Сетбаккупоптионс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**Ивсскомпонент:: Жетбаккупоптионс**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**Ивссбаккупкомпонентс:: Сетрестореоптионс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**Ивсскомпонент:: Жетрестореоптионс**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Сообщения о сбое: <dl>

[**Ивсскомпонент:: Сетпостресторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**Ивсскомпонент:: Сетпрересторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**Ивсскомпонент:: Сетпостресторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**Ивсскомпонент:: Сетпрересторефаилуремсг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Целевые объекты восстановления: <dl>

[**Ивсскомпонент:: Сетресторетаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**Ивсскомпонент:: Жетресторетаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Метки резервного копирования: <dl>

[**Ивсскомпонент:: Сетбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**Ивсскомпонент:: Жетбаккупстамп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Дополнительные метаданные: <dl>

[**Ивсскомпонент:: Сетрестореметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**Ивсскомпонент:: Жетрестореметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**Ивсскомпонент:: Сетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**Ивсскомпонент:: Жетбаккупметадата**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Поэтому используется экземпляр интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) в определяющем члене набора компонентов или используется имя, тип и логический путь определяющего члена с методом [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) для установки или получения свойств всех членов набора компонентов.

По этой причине Наборы компонентов обрабатываются как единицы измерения. Например, резервная копия набора компонентов завершается успешно, только если резервное копирование всех наборов файлов всех его компонентов прошло успешно.

В предыдущем примере предположим, что один файл в компоненте «Jan» (с логическим путем «Вритердата \\ Set2») является членом набора компонентов, определенного параметром «вритердата». Если не удалось выполнить резервное копирование одного из файлов "Jan", запрашивающая сторона будет использовать сведения "Вритердата" (имя "Вритердата", путь "" и тип компонента) в качестве аргументов при задании [**ивссбаккупкомпонентс:: сетбаккупсукцеедед**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) с **false** для указания на сбой набора компонентов.

Аналогично, состояние, возвращаемое [**ивсскомпонент:: жетбаккупсукцеедед**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) для экземпляра Вритердата интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , применяется не только к "вритердата", но и ко всем его подкомпонентам.

Кроме того, если модуль записи решил изменить цель восстановления с помощью [**ивсскомпонент:: сетресторетаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) экземпляра вритердата [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent), то он изменит целевой объект восстановления для всех наборов файлов всех подкомпонентов "вритердата".

Следующие свойства применяются не ко всему компоненту, а к определенным файлам или наборам файлов:

-   Сопоставления альтернативного расположения: <dl>

[**Ивссбаккупкомпонентс:: Аддалтернативелокатионмаппинг**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**Ивсскомпонент:: Жеталтернателокатионмаппинг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**Ивсскомпонент:: Жеталтернателокатионмаппингкаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Разностные файлы: <dl>

[**Ивсскомпонент:: Адддифференцедфилесбиластмодифитиме**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**Ивсскомпонент:: Жетдифференцедфиле**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**Ивсскомпонент:: Жетдифференцедфилескаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   Частичные файлы: <dl>

[**Ивсскомпонент:: Аддпартиалфиле**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**Ивсскомпонент:: Жетпартиалфиле**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**Ивсскомпонент:: Жетпартиалфилекаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Направленные целевые объекты: <dl>

[**Ивсскомпонент:: Адддиректедтаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**Ивсскомпонент:: Жетдиректедтаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**Ивсскомпонент:: Жетдиректедтаржеткаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Новые целевые объекты: <dl>

[**Ивссбаккупкомпонентс:: Аддневтаржет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**Ивсскомпонент:: Жетневтаржет**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**Ивсскомпонент:: Жетневтаржеткаунт**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Когда инициатор запроса обращается к этим функциям для подкомпонента с помощью интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , он использует сведения о компоненте для компонента, определяющего набор компонентов, но сведения о файле или наборе файлов для подкомпонента.

Аналогично, если свойство доступно через интерфейс [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , используется экземпляр, соответствующий определяющему подкомпоненту, но аргументы файла или набора файлов берутся из подкомпонента.

Например, предположим, что подкомпоненту «Jan» (с логическим путем «Вритердата \\ Set2») присвоено множество файлов с путем «c: \\ Fred», спецификация файла « \* . dat», а рекурсивный флаг « **Истина** » может быть восстановлен в альтернативное расположение.

В этом случае инициатор запроса вызовет [**ивссбаккупкомпонентс:: аддалтернативелокатионмаппинг**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping), используя сведения об "вритердата" (тип компонента, имя компонента "writeData" и логический путь ""), а также сведения о наборе файлов "Jan" (путь "c: \\ Fred", спецификация файла " \* . dat", а рекурсия — **true**).

Обратите внимание, что в этом случае сведения о наборе файлов должны точно соответствовать сведениям о наборе файлов, используемых [**ивсскреатевритерметадата:: аддфилестофилеграуп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**Ивсскреатевритерметадата:: адддатабасефилес**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)или [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) для добавления файлов в Jan.

Аналогично, если модуль записи хочет добавить направленный целевой объект в файл с путем "c: \\ есел" и именем "Люси. dat", управляемый с помощью "Jan" (с логическим путем "вритердата \\ Set2"), будет использоваться экземпляр [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , соответствующий "вритердата", но сведения о файле "Jan".

## <a name="implicitly-included-components-in-the-restore-set"></a>Неявно включаемые компоненты в набор восстановления

Компоненты, которые были неявно включены в резервную копию, могут быть явно включены в восстановление, если они могут быть выбраны для восстановления. Как отмечалось при [работе с выборкой для восстановления и подкомпонентов](working-with-selectability-for-restore-and-subcomponents.md), такие компоненты добавляются в документ компонентов резервного копирования с помощью метода [**Ивссбаккупкомпонентс:: аддресторесубкомпонент**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) .

Однако это не создает новый экземпляр интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , а также компонент, напрямую доступный через интерфейс [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Вместо этого компонент, явно включаемый в восстановление, но неявно включаемый для резервного копирования, должен быть доступен через экземпляр интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , соответствующий компоненту, который определил, что он был членом при резервном копировании.

Например, чтобы явно включить для Restore "set1", подкомпонент выбираемого компонента для резервного копирования "Вритердата", необходимо получить сведения о нем, вызвав метод [**ивсскомпонент:: жетресторесубкомпонент**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) экземпляра Вритердата интерфейса [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

 

 



