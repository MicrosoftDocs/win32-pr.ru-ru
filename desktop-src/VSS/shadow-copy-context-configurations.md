---
description: Запрашивающие стороны управляют функциями теневой копии, задавая ее контекст. Этот контекст указывает, будет ли теневая копия содержаться в текущей операции, а также степенью координации модуля записи и поставщика.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Конфигурации контекста теневого копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e156b0357813060adcc3e7e8b5072b7a17543b7c996db72686a4912f504fede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937766"
---
# <a name="shadow-copy-context-configurations"></a>Конфигурации контекста теневого копирования

Запрашивающие стороны управляют функциями теневой копии, задавая ее контекст. Этот контекст указывает, будет ли теневая копия содержаться в текущей операции, а также степенью координации модуля записи и поставщика.

## <a name="persistence-and-shadow-copy-context"></a>Контекст сохраняемости и теневого копирования

Теневая копия может быть [*постоянной*](vssgloss-p.md), т. е. теневая копия не удаляется после завершения операции резервного копирования или выпуска объекта [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Для постоянных теневых копий требуются [**\_ \_ \_ контексты контекста моментальных снимков**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) VSS **\_ CTX \_ клиента \_ VSS**, **\_ \_ \_ откат приложения VSS CTX** или **\_ \_ \_ откат VSS CTX NAS**. Постоянные теневые копии можно создавать только для томов NTFS.

Непостоянные теневые копии создаются с использованием контекстов **\_ \_ резервного копирования VSS CTX** или **VSS \_ CTX \_ файлового \_ ресурса \_**. Для NTFS и томов, отличных от NTFS, можно создавать непостоянные теневые копии.

## <a name="writer-participation-and-shadow-copies"></a>Участие в записи и теневые копии

Контекст теневой копии может классифицироваться либо с участием модулей записи, либо без участия в модулях записи.

Контексты теневого копирования, которые включают в себя записи для создания, включают:

-   **\_ \_ откат приложения CTX \_ VSS**
-   **\_ \_ резервное копирование CTX VSS**
-   **\_ \_ \_ модули записи, доступные \_ клиенту VSS CTX**

Те, которые не включают в себя модули записи при их создании, включают:

-   **\_доступ к \_ клиенту \_ CTX VSS**
-   **\_ \_ \_ резервное копирование файлового ресурса CTX VSS \_**
-   **\_откат CTX \_ NAS \_ VSS**

Один контекст может использоваться с обоими типами теневых копий, но не может использоваться при создании теневой копии:

-   **VSS \_ CTX \_ все**

Создание теневой копии с помощью контекста **VSS \_ CTX \_ ALL** (с использованием [**Ивссбаккупкомпонентс:: Стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) и [**ивссбаккупкомпонентс::D оснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) не поддерживается.

Операции, поддерживающие контекст **VSS \_ CTX \_ ALL** , — это административные операции [**ивссбаккупкомпонентс:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**ивссбаккупкомпонентс::D Елетеснапшотс**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**ивссбаккупкомпонентс:: бреакснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)и [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).

## <a name="obtaining-shadow-copy-information"></a>Получение сведений о теневой копии

Если инициатор запроса знает идентификационный идентификатор GUID теневой копии (ее **\_ идентификатор VSS**), он может получить сведения о контексте определенной теневой копии (определяется ее **\_ идентификатором VSS**) путем распаковки структуры свойства " [**\_ \_ prop" моментального снимка VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , возвращенной вызовом метода [**ивссбаккупкомпонентс:: жетснапшотпропертиес**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Чтобы получить контекстные сведения обо всех теневых копиях в системе, инициатор запроса изучает **член m \_ Лснапшотаттрибутес** элемента **obj. Snap** в [**\_ \_ свойстве-объекте Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) . Snapin (структура [**\_ снимка VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ), полученном с помощью [**ивссенумобжект**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) , для прохода по списку объектов, возвращенных вызовом [**ивссбаккупкомпонентс:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

 

 



