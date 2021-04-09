---
description: Задает относительный приоритет потока для ветви топологии.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154982"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>\_ \_ \_ \_ Атрибут приоритета MMCSS топоноде ворккуеуе MF

Задает относительный приоритет потока для ветви топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**). Атрибут является необязательным.

Для этого атрибута требуются атрибуты класса [MF \_ топоноде \_ Ворккуеуе \_ ID](mf-toponode-workqueue-id-attribute.md) и [MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) на одном узле.

Значение атрибута — это относительный приоритет потока рабочей очереди для этой ветви топологии. [Служба диспетчера классов мультимедиа](../procthread/multimedia-class-scheduler-service.md) (MMCSS) использует относительный приоритет, если он задает приоритет потока. Дополнительные сведения см. в разделе [**авсетммсреадприорити**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> <dt>

[Усовершенствования рабочей очереди и потоков](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
