---
description: Существует несколько различных типов теневых копий, которые может создать инициатор запроса.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Создание простой теневой копии для резервного копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f9cda7a2d2679979879a2333b30621fb7f73a449f4a15b55b42c603cd913713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394174"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Создание простой теневой копии для резервного копирования

Существует несколько различных типов теневых копий, которые может создать инициатор запроса. Однако для большинства приложений резервного копирования необходимо выполнить следующие действия.

1.  Вызовите [**ивссбаккупкомпонентс:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) с контекстом \_ \_ резервного копирования VSS CTX.
2.  Вызовите метод [**ивссбаккупкомпонентс:: гасервритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , чтобы инициализировать обмен данными с модулями записи.
3.  Вызовите метод [**ивссбаккупкомпонентс:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , чтобы добавить файл и компоненты базы данных в резервную копию.
4.  Вызовите метод [**ивссбаккупкомпонентс:: стартснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) , чтобы инициализировать механизм теневого копирования.
5.  Вызовите [**ивссбаккупкомпонентс:: аддтоснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) , чтобы включить тома в теневую копию.
6.  Вызовите [**ивссбаккупкомпонентс::P репарефорбаккуп**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) , чтобы уведомить модули записи об операциях резервного копирования.

 

 



