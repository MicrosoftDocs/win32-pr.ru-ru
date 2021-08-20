---
description: Представляет сведения, поддерживаемые диспетчером секций, о диске, входящем в состав кластера.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: Структура DISK_CLUSTER_INFO (Нтдддиск. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: be4db89e888778c3d92090a32243f0203b527337b3734328a183b551a6181f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813796"
---
# <a name="disk_cluster_info-structure"></a>\_ \_ Структура сведений о КЛАСТЕРе диска

Представляет сведения, поддерживаемые диспетчером секций, о диске, входящем в состав кластера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Version**
</dt> <dd>

Номер версии. Это значение должно быть равно размеру этой структуры.

</dd> <dt>

**Флаги**
</dt> <dd>

Сочетание флагов, связанных с дисками и кластерами.



| Значение                                                                                                                                                                                                                                                                                               | Значение                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**Диск \_ \_Флаг кластера \_ включен**</dt> <dt>1</dt> </dl>                                          | Диск используется как часть службы кластеров.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**Диск \_ \_Флаг кластера \_ CSV**</dt> <dt>2</dt> </dl>                                                      | Тома на диске публикуются CSVFS на всех узлах кластера.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**Диск \_ \_Флаг кластера \_ в \_ обслуживании**</dt> <dt>4</dt> </dl>                    | Ресурс кластера, связанный с этим диском, находится в режиме обслуживания.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**Диск \_ Установка \_ флага кластера о \_ \_ получении PnP \_ завершена**</dt> <dt>8</dt> </dl> | Драйвер диска кластера для режима ядра (Clusdisk) получил уведомление PnP о поступлении диска.<br/> |



 

</dd> <dt>

**флагсмаск**
</dt> <dd>

Флаги, изменяемые в элементе **flags** .

</dd> <dt>

**Уведомление**
</dt> <dd>

**Значение true** , чтобы отправить уведомление об изменении макета; в противном случае — **значение false**.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Нтдддиск. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры управления дисками](disk-management-structures.md)
</dt> <dt>

[**IOCTL \_ Disk \_ Получение \_ \_ сведений о кластере**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**\_ \_ сведения о наборе дисков для \_ кластера ioctl \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




