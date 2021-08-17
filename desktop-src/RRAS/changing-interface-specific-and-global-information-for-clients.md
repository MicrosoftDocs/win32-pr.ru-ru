---
title: Изменение Interface-Specific и глобальных сведений для клиентов
description: Чтобы изменить сведения об интерфейсе для конкретного клиента, например NAT, сначала используйте соответствующий параметр \ 0034; Сведения \ 0034; Функция для получения текущих данных.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcea02c6d70e7d7e2da53926854879f1ca5b76526a83185b786b0074b8098434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791757"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Изменение Interface-Specific и глобальных сведений для клиентов

Чтобы изменить сведения об интерфейсе для конкретного клиента, например NAT, сначала используйте соответствующую функцию "с информацией" для получения текущих данных. Если маршрутизатор работает, используйте [**мпрадмининтерфацетранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Если маршрутизатор не работает, используйте [**мпрконфигинтерфацетранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Этот вызов извлекает сведения обо всех клиентах, работающих на указанном интерфейсе. Например, если и OSPF, и RIP выполняются на определенном интерфейсе, этот вызов получает сведения об интерфейсе для обоих. Используйте функцию [**мпринфоблоккфинд**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) для нахождение информационного блока, соответствующего клиенту, который необходимо изменить. Затем используйте функцию [**мпринфоблокксет**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) для выполнения изменений. Наконец, используйте [**мпрадмининтерфацетранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) или [**мпрконфигинтерфацесетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) , чтобы внести изменения в выполняющийся маршрутизатор или конфигурацию маршрутизатора в реестре.

Сведения о глобальном клиенте — это сведения, не относящиеся к конкретному интерфейсу, на котором работает клиент. Аналогичная процедура используется для изменения глобальных данных для конкретного клиента. Сначала получите глобальные сведения для всех клиентов, использующих [**мпрадминтранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) или [**мпрконфигтранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo). Затем используйте функции Мпринфо для изменения информации. Наконец, используйте функции [**мпрадминтранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) или [**мпрконфигтранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) , чтобы сохранить измененные сведения обратно на работающем маршрутизаторе или в реестре.

Вызовы к предыдущим функциям администрирования проходят через диспетчер динамического интерфейса (DIM) и в конечном итоге преобразуют их в вызовы от диспетчера маршрутизатора к самим клиентам. Все клиенты, независимо от того, являются ли они протоколами маршрутизации, должны соответствовать интерфейсу, описанному в разделе [интерфейс протокола маршрутизатора](about-routing-protocol-interface.md). В рамках этого интерфейса протокол маршрутизации должен поддерживать следующие функции (Кроме других):

-   [**жетглобалинфо**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**сетглобалинфо**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**жетинтерфацеинфо**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**сетинтерфацеинфо**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

Диспетчер маршрутизаторов вызывает функции [**жетинтерфацеинфо**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) для каждого клиента, чтобы собрать сведения, возвращаемые при вызове функции [**мпрадмининтерфацетранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Аналогично, когда диспетчер маршрутизатора получает обновленные сведения через вызов [**мпрадмининтерфацетранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) , он использует функции [**сетинтерфацеинфо**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) для обновления сведений об интерфейсе для каждого из клиентов.

 

 




