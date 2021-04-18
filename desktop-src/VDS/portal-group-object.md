---
description: Объект группы портала
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Объект группы портала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546895"
---
# <a name="portal-group-object"></a>Объект группы портала

\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Объект группы портала моделирует группу порталов iSCSI, содержащуюся в целевом объекте iSCSI.

Используйте метод [**ивдсискситаржет:: куерипорталграупс**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) , чтобы определить группы порталов, содержащиеся в определенном целевом объекте. Используйте метод [**ивдсисксипортал:: куеряссоЦиатедпорталграупс**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) , чтобы определить группы порталов, связанные с указанным порталом. Вызывающие объекты могут получить указатель на определенную группу портала, выбрав нужный объект группы портала из перечисления, возвращаемого методом **куерипорталграупс** или методом **куеряссоЦиатедпорталграупс** . С помощью объекта группы портал можно добавлять или удалять порталы и запросы к свойствам групп порталов, связанным порталам и целевым объектам, содержащим группу порталов.

Свойства объекта группы портала включают [идентификатор объекта](vds-data-types.md) и тег группы портала. Дополнительные сведения о тегах группы порталов см. в спецификации iSCSI по адресу <https://go.microsoft.com/fwlink/p/?linkid=158752> .

В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.



| Тип                                                                                      | Элемент                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы, которые всегда предоставляются этим объектом в поставщиках iSCSI для VDS 1,1 и 2,0 | [**Ивдсисксипорталграуп**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Связанные перечисления                                                                   | Нет.                                                                                                                                              |
| Связанные структуры                                                                     | Служба [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) [**\_ \_ \_ Уведомление группы**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)порталграуп iSCSI и портала VDS. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объекты поставщика оборудования](hardware-provider-objects.md)
</dt> <dt>

[**Ивдсисксипортал:: КуеряссоЦиатедпорталграупс**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**Ивдсискситаржет:: Куерипорталграупс**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
