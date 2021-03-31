---
description: Существует несколько различных типов теневых копий, которые может создать инициатор запроса.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Создание простой теневой копии для резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809424"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Создание простой теневой копии для резервного копирования

Существует несколько различных типов теневых копий, которые может создать инициатор запроса. Однако для большинства приложений резервного копирования необходимо выполнить следующие действия.

1.  Вызовите [**ивссбаккупкомпонентс:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) с контекстом \_ \_ резервного копирования VSS CTX.
2.  Вызовите метод [**ивссбаккупкомпонентс:: гасервритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , чтобы инициализировать обмен данными с модулями записи.
3.  Вызовите метод [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , чтобы добавить файл и компоненты базы данных в резервную копию.
4.  Вызовите метод [**ивссбаккупкомпонентс:: стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) , чтобы инициализировать механизм теневого копирования.
5.  Вызовите [**ивссбаккупкомпонентс:: аддтоснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) , чтобы включить тома в теневую копию.
6.  Вызовите [**ивссбаккупкомпонентс::P репарефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) , чтобы уведомить модули записи об операциях резервного копирования.

 

 



