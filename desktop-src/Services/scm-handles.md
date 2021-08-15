---
description: SCM поддерживает типы Handles, чтобы разрешить доступ к следующим объектам.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Дескрипторы SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6830063e57b2135c32bf01b4fdc0b4cf6207de32198d9f88d97667f4b403fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889192"
---
# <a name="scm-handles"></a>Дескрипторы SCM

SCM поддерживает типы Handles, чтобы разрешить доступ к следующим объектам.

-   База данных установленных служб.
-   Служба.
-   Блокировка базы данных.

Объект SCManager представляет базу данных установленных служб. Это объект контейнера, который содержит объекты службы. Функция [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) возвращает маркер объекта SCManager на указанном компьютере. Этот маркер используется при установке, удалении, открытии и перечислении служб, а также при блокировке базы данных служб.

Объект службы представляет установленную службу. Функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) и [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) возвращают дескрипторы для установленных служб.

Функции [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)и [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) могут запрашивать различные типы доступа к SCManager и объектам службы. Запрошенный доступ предоставляется или отклоняется в зависимости от маркера доступа вызывающего процесса и дескриптора безопасности, связанного с объектом SCManager или Service.

Функция [**клосесервицехандле**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) закрывает дескрипторы SCManager и объектов службы. Если эти дескрипторы больше не нужны, закройте их.

 

 



