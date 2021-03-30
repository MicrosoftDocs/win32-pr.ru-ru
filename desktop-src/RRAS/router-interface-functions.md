---
title: Функции интерфейса маршрутизатора
description: Используйте следующие функции для администрирования интерфейсов на маршрутизаторе.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328232"
---
# <a name="router-interface-functions"></a>Функции интерфейса маршрутизатора

Используйте следующие функции для администрирования интерфейсов на маршрутизаторе.



| Функция администрирования                                          | Функция настройки                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**мпрадмининтерфацекреате**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**мпрконфигинтерфацекреате**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**мпрадмининтерфацеделете**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**мпрконфигинтерфацеделете**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**мпрадмининтерфацеенум**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**мпрконфигинтерфацеенум**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**мпрадмининтерфацежесандле**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**мпрконфигинтерфацежесандле**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**мпрадмининтерфацежетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**мпрконфигинтерфацежетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**мпрадмининтерфацесетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**мпрконфигинтерфацесетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

Эти функции влияют на сами интерфейсы, а не на клиенты, работающие в интерфейсах. По этой причине ни одна из функций не требует от вызывающей стороны указания конкретного транспорта (IP или IPX); Хотя клиенты (например, протоколы маршрутизации) связаны с определенными транспортами, сами интерфейсы не являются.

Эти функции непосредственно обрабатываются с помощью DIM. Они не используют диспетчеры маршрутизаторов.

Функции [**мпрадмининтерфацекреате**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) и [**мпрадмининтерфацеделете**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) не могут создавать или удалять интерфейсы локальной сети. Они могут только создавать или удалять интерфейсы вызова по требованию. Список типов интерфейсов см. в разделе [**\_ \_ тип интерфейса маршрутизатора**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) .

 

 




