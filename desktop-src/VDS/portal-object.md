---
description: Объект Portal
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Объект Portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7004f648b11b16c8c6279a0a74bae775fa539d8f0a93fc83d7effccea68915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864524"
---
# <a name="portal-object"></a>Объект Portal

\[начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API Windows служба хранилища управления](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Объект портала моделирует портал iSCSI, содержащийся в подсистеме iSCSI.

Чтобы определить порталы iSCSI подсистемы, используйте метод [**ивдссубсистемискси:: куерипорталс**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) . Вызывающие объекты могут получить указатель на конкретный портал, выбрав нужный объект портала из перечисления, возвращаемого методом **куерипорталс** . С помощью объекта портала можно задать состояние портала и запрос свойств портала, связанных групп портала и подсистемы, содержащей портал.

Объект портала может быть связан только с одной группой портала указанного целевого объекта.

Порталы служат одной из конечных точек путей MPIO в поставщиках оборудования iSCSI, на которых можно налагать политики балансировки нагрузки.

К свойствам объекта портала относятся идентификатор объекта, IP-адрес и порт, а также состояние портала.

В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.



| Тип                                                                                      | Элемент                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы, которые всегда предоставляются этим объектом в поставщиках iSCSI для VDS 1,1 и 2,0 | [**Ивдсисксипортал**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Связанные перечисления                                                                   | Служба [**VDS \_ \_ \_ состояние портала iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).                                                          |
| Связанные структуры                                                                     | Служба [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) [**\_ \_ Уведомление о портах и службе VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)портала iSCSI. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объекты поставщика оборудования](hardware-provider-objects.md)
</dt> <dt>

[**Ивдссубсистемискси:: Куерипорталс**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
