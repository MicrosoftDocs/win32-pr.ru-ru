---
title: Функции интерфейса маршрутизатора
description: Используйте следующие функции для администрирования интерфейсов на маршрутизаторе.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcaaf257e31623036a075c21da66d4665b3afe7e821f8f246f6a225e02b8272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787840"
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

 

 




