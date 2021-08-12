---
description: Уведомления службы VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Уведомления службы VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931731cc9c2b4aa73f7599c1fcbfad2f885bc74978ab15ba4e1efbf9d2a7522c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603120"
---
# <a name="vds-notifications"></a>Уведомления службы VDS

\[начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API Windows служба хранилища управления](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Поставщик может отправлять уведомления о событиях в службу VDS, а служба VDS может пересылать уведомления в приложения. Модель уведомления, используемая службой VDS, похожа на модель точки подключения, используемую объектами COM.

Служба VDS создает уведомления службы для таких событий, как назначение буквы диска или поступление невыделенного диска. После того как служба VDS выделяет диск поставщику, поставщик отвечает за создание связанных уведомлений. На рисунке ниже показаны интерфейсы и методы, используемые в модели уведомлений VDS.

![Схема, на которой показаны интерфейс и методы (advise, OnLoad и OnLoad) между приложениями, службой виртуальных дисков и поставщиками V D S.](images/vdsnotification.png)

Для получения уведомлений служба VDS регистрирует свой интерфейс [**ивдсадвисесинк**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) в объекте поставщика, вызывая метод [**ивдспровидерпривате:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) и передавая указатель на интерфейс. При возникновении события уведомления, например о поступлении нового тома или диска, поставщик передает соответствующую структуру уведомлений службе VDS в качестве параметра метода [**ивдсадвисесинк:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

Процесс аналогичен для приложения и VDS. В частности, для получения уведомлений приложение регистрирует свой интерфейс [**ивдсадвисесинк**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) с помощью VDS, вызывая метод [**Ивдссервице:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) и передавая указатель на интерфейс. Когда служба VDS получает уведомление от поставщика, она передает соответствующую структуру уведомлений в зарегистрированные приложения как параметр метода [**ивдсадвисесинк:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

> [!Note]  
> Приложение, вызывающее предложение [**advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) , должно в конечном итоге вызвать метод [**ивдссервице:: unadvise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) . В идеале следует вызывать метод **unadvise** , как только больше не требуется получать уведомления.

 

В следующей таблице перечислены уведомления, созданные поставщиком по типу объектов.



| Объект     | Уведомление                              | Значение | Ссылка на описание события                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **получение \_ пакета NF для службы VDS \_ \_**                 | 1     | [**\_уведомление пакета \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **Служба VDS \_ NF \_ Pack \_ выбывают**                 | 2     | [**\_уведомление пакета \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **\_ \_ изменение пакета NF для VDS \_**                 | 3     | [**\_уведомление пакета \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Громкость     | **получение \_ тома NF для службы VDS \_ \_**               | 4     | [**\_уведомление тома \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Громкость     | **Служба VDS \_ NF \_ Volume \_ выбывают**               | 5     | [**\_уведомление тома \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Громкость     | **\_ \_ изменение тома NF для службы VDS \_**               | 6     | [**\_уведомление тома \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Громкость     | **\_ \_ \_ ход перестроения тома NF службы VDS \_** | 7     | [**\_уведомление тома \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Диск       | **\_приприбытие \_ диска NF VDS \_**                 | 8     | [**\_уведомление диска службы VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Диск       | **Служба VDS \_ NF \_ Disk \_ выбывают**                 | 9     | [**\_уведомление диска службы VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Диск       | **Служба VDS \_ NF, \_ \_ Изменение диска**                 | 10    | [**\_уведомление диска службы VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Секция  | **получение \_ Секции NF для службы VDS \_ \_**            | 11    | [**\_ \_ уведомление о разделе VDS**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Секция  | **Служба VDS \_ NF \_ Partition \_ выбывают**            | 12    | [**\_ \_ уведомление о разделе VDS**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Секция  | **\_ \_ изменение раздела NF для службы VDS \_**            | 13    | [**\_ \_ уведомление о разделе VDS**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **\_доприбытие \_ \_ подсистемы \_ VDS NF**          | 101   | [**\_ \_ уведомление ПОДсистемы \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **Подсистема NF для VDS \_ \_ \_ \_ выбывают**          | 102   | [**\_ \_ уведомление ПОДсистемы \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **\_ \_ \_ изменение подсистемы службы VDS NF \_**          | 151   | [**\_ \_ уведомление ПОДсистемы \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Контроллер | **получение \_ контроллера NF для службы VDS \_ \_**           | 103   | [**\_уведомление контроллера \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Контроллер | **\_NF \_ контроллера VDS \_ выбывают**           | 104   | [**\_уведомление контроллера \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Контроллер | **\_ \_ Изменение контроллера NF для службы VDS \_**           | 350   | [**\_уведомление контроллера \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Контроллер | **\_контроллер NF \_ VDS \_ удален**          | 351   | [**\_уведомление контроллера \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Порт       | **\_ \_ изменение порта NF службы VDS \_**                 | 352   | [**\_уведомление порта \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Порт       | **\_порт NF службы VDS \_ \_ удален**                | 353   | [**\_уведомление порта \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Накопитель      | **\_приприбытие \_ диска NF VDS \_**                | 105   | [**\_уведомление диска \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Накопитель      | **Служба VDS \_ NF \_ диск \_ выбывают**                | 106   | [**\_уведомление диска \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Накопитель      | **Служба VDS \_ NF \_ диск \_ изменить**                | 107   | [**\_уведомление диска \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Накопитель      | **\_диск NF \_ VDS \_ удален**               | 354   | [**\_уведомление диска \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **получение \_ LUN NF для VDS \_ \_**                  | 108   | [**\_уведомление LUN \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **\_NF \_ LUN VDS \_ выбывают**                  | 109   | [**\_уведомление LUN \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **Служба VDS \_ NF \_ LUN \_ Modify**                  | 110   | [**\_уведомление LUN \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

Служба VDS создает остальные уведомления. В следующей таблице перечислены константы уведомлений на основе служб по категориям.



| Категория     | Уведомление                                | Значение | Ссылка на описание события                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Диск         | **\_приприбытие \_ диска NF VDS \_**                   | 8     | [**\_уведомление диска службы VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Диск         | **Служба VDS \_ NF \_ Disk \_ выбывают**                   | 9     | [**\_уведомление диска службы VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Диск         | **Служба VDS \_ NF, \_ \_ Изменение диска**                   | 10    | [**\_уведомление диска службы VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Буква диска | **\_ \_ \_ бесплатная буква диска NF VDS \_**            | 201   | [**\_ \_ уведомление о букве диска VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Буква диска | **\_ \_ \_ Назначение буквы диска NF \_ VDS**          | 202   | [**\_ \_ уведомление о букве диска VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Файловая система  | **\_ \_ \_ изменение файловой системы \_ службы VDS NF**           | 203   | [**\_уведомление файловой \_ системы \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Файловая система  | **\_ \_ \_ \_ ход выполнения форматирования файловой системы \_ службы VDS NF** | 204   | [**\_уведомление файловой \_ системы \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Громкость       | **\_ \_ \_ изменение точек подключения службы VDS NF \_**          | 205   | [**\_ \_ уведомление точки подключения \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объектная модель VDS](vds-object-model.md)
</dt> <dt>

[**ивдсадвисесинк**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**Ивдсадвисесинк:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**Ивдспровидерпривате:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**Ивдссервице:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
