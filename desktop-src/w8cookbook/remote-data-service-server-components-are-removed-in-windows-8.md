---
title: Удаленная служба данных удалена
description: Удаленные компоненты сервера удаленной службы данных в Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Сервер RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "103987952"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>Удаленные компоненты сервера удаленной службы данных в Windows 8

## <a name="platforms"></a>Платформы

 **Клиенты** — Windows 8  
**Серверы** — Windows Server 2012  



## <a name="description"></a>Описание

Сервер удаленной службы данных (RDS) недоступен в Windows 8:

-   Файл msadcf.dll, в котором размещается по умолчанию "бизнес-объект" RDSServer. DataObject, удаляется, а связанные с ним файлы (msadcfr.dll, msadcfr.dll. MUI, handler. reg и хандсафе. reg) удаляются.
-   Файл msdfmap.dll, который является обработчиком по умолчанию, удаляется, а файл msdfmap.ini удаляется.
-   Файл msadcs.dll, ISAPI, удален

## <a name="manifestation"></a>Проявление

Клиенты не могут размещать RDS Server в Windows 8.

## <a name="mitigation"></a>Меры по снижению риска

Клиенты могут размещать свои RDS-серверы на компьютере с Windows 7 или с другими операционными системами нижнего уровня.

## <a name="solution"></a>Решение

Клиенты могут размещать свои RDS-серверы на компьютере с Windows 7 или с другими операционными системами нижнего уровня.

## <a name="resources"></a>Ресурсы

[Схема технологий доступа к данным](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 