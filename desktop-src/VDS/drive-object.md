---
description: Объект Drive
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Объект Drive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04ec68fab408c4ed6412990296c0ebb265b8c3e4c4c9b05645b1f4bd1e625fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603424"
---
# <a name="drive-object"></a>Объект Drive

\[начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API Windows служба хранилища управления](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Объект Drive моделирует физический диск, содержащийся в подсистеме. Каждый диск подключается к шине, занимает слот и содержит набор экстентов диска. Каждый диск может добавлять экстенты в любое количество LUN. Диск также можно назначить горячим резервом.

Используйте метод [**ивдссубсистем:: куеридривес**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) , чтобы определить диски, содержащиеся в определенной подсистеме. Вызывающие объекты могут получить указатель на конкретный диск, выбрав нужный объект диска из перечисления, возвращаемого методом **куеридривес** , или вызвав метод [**ивдссубсистем::**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) GetObject и передав требуемую шину и номер слота. С помощью объекта Drive можно задать состояние диска и запрос свойств диска, связанных областей диска и подсистемы, содержащей диск.

В дополнение к идентификатору объекта, имени и серийному номеру свойства объекта диска включают состояние диска, работоспособность и флаги. Размер в байтах; и номер шины и разъема.

В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.



| Тип                                              | Элемент                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы, которые всегда предоставляются этим объектом | [**ивдсдриве**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Интерфейсы, которые могут предоставляться этим объектом     | [**ивдсмаинтенанце**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Связанные перечисления                           | Служба [**VDS \_ \_Флаг диска**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ состояние диска VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)и [**\_ \_ экстент диска VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Связанные структуры                             | Служба [**VDS \_ Уведомление \_ Drive**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) и [**\_ устройство VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объекты поставщика оборудования](hardware-provider-objects.md)
</dt> <dt>

[**Ивдссубсистем:: Куеридривес**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**Ивдссубсистем:: OverDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
