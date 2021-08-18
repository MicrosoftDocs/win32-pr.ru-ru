---
description: События прерывания могут создаваться во время операции резервного копирования в любом из следующих случаев.
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Прерывание операций VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120ef8fb16c23d77a24526aad0fd62e56c1888a76dc2de884140094c6591cd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998274"
---
# <a name="aborting-vss-operations"></a>Прерывание операций VSS

События [*прерывания*](vssgloss-a.md) могут создаваться во время операции резервного копирования в любом из следующих случаев.

-   Инициатор запроса явно создает [*событие Abort*](vssgloss-a.md) , вызывая [**Ивссбаккупкомпонентс:: абортбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   Обработчики событий [*Freeze*](vssgloss-f.md) и [*разморозки*](vssgloss-t.md) модуля записи ([**квссвритер:: onfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) и [**квссвритер:: размораживание**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) возвращают **значение false** или не могут быть завершены в временном окне, указанном в [**квссвритер:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize).
-   При создании теневой копии после события [*препарефорснапшот*](vssgloss-p.md) возникает ошибка поставщика или VSS.

Для операций восстановления не поддерживаются прерывания.

## <a name="requester-handling-and-creation-of-abort-events"></a>Обработка и создание запросов событий прерывания

Экземпляр интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) можно использовать только для одной резервной копии, поэтому, если при обработке резервной копии возникает ошибка, лучше всего освободить текущий экземпляр и начать заново.

Инициатор запроса должен явно сообщить, что операция резервного копирования прервана (с помощью [**ивссбаккупкомпонентс:: абортбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) только после фактической подготовки к резервному копированию, включающей модули записи или создания теневой копии.

Фактически, это означает, что каждый раз, когда инициатору запроса требуется прерывать операцию резервного копирования после создания события [*PrepareForBackup*](vssgloss-p.md) путем вызова [**Ивссбаккупкомпонентс::P репарефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), он должен вызвать [**ивссбаккупкомпонентс:: абортбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) и ожидать его возврата до освобождения текущего экземпляра [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Например, если модуль записи запретил операцию резервного копирования, запрашивающая сторона должна использовать [**ивссбаккупкомпонентс:: абортбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) для уведомления всех остальных модулей записи о том, что операция резервного копирования не будет завершена.

Перед вызовом [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)или при сбое вызова **PrepareForBackup** инициатор запроса может освободить текущий экземпляр интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , не требуя создания события прерывания.

Например, если текущий экземпляр [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) используется только для получения информации путем вызова [**Ивссбаккупкомпонентс:: гасервритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) и создания события [*определения*](vssgloss-i.md) , после того как информация возвращена, экземпляр **ивссбаккупкомпонентс** можно просто освободить.

Инициатор запроса создает ряд событий ([*препарефорснапшот*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*разморозить*](vssgloss-t.md)и [*моментальный снимок*](vssgloss-p.md)) при вызове [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). При обработке событий замораживания и разморозки может произойти сбой модуля записи, и можно создать событие прерывания самостоятельно. Сбой при обработке событий Препарефорснапшот и SNAPSHOT не приводит к созданию события прерывания.

Не всегда возможно, что инициатору запроса известно, было ли событие Abort создано, когда [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) указывает на ошибку. Таким образом, инициатор запроса, которому требуется завершить операцию резервного копирования, потому что состояние **ивссбаккупкомпонентс::D оснапшотсет** указывает, что проблема все равно должна вызывать [**Ивссбаккупкомпонентс:: абортбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Если запросивший объект вызвал [**ивссбаккупкомпонентс:: абортбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), то перед освобождением экземпляра [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)не нужно вызывать [**ивссбаккупкомпонентс:: баккупкомплете**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) .

## <a name="writer-handling-and-creation-of-abort-events"></a>Обработка и создание событий прерывания записи

Как отмечалось ранее, модуль записи может получить событие прерывания от инициатора запроса или поставщик может активировать его. Кроме того, при определенных обстоятельствах средство записи может принимать несколько событий прерывания. Разработчикам модуля записи следует запрограммировать любую реализацию [**квссвритер:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) с учетом этого.

При обработке события прерывания модуль записи должен попытаться восстановить все управляемые им процессы в нормальном состоянии, а также выполнять обработку ошибок и ведение журнала.

Это может означать, что реализация [**квссвритер:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) может потребоваться выполнить многие из тех же задач, что и обработчик событий разморозки ([**квссвритер:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)), и обработчик событий моментального снимка ([**квссвритер:: онпостснапшот**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)), и эти обработчики можно вызывать из **квссвритер:: OnAbort**.

 

 



