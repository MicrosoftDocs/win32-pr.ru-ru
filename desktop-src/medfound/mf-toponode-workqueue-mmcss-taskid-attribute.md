---
description: Указывает идентификатор задачи службы планировщика классов мультимедиа (MMCSS) для ветви топологии.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543239"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>\_Атрибут MF топоноде \_ ворккуеуе \_ MMCSS \_

Указывает идентификатор задачи службы планировщика классов мультимедиа (MMCSS) для ветви топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**). Этот атрибут является необязательным.

Этот атрибут игнорируется, если не заданы также следующие атрибуты:

-   [**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**](mf-toponode-workqueue-id-attribute.md)
-   [**\_ \_ \_ класс MMCSS ТОПОНОДЕ ворккуеуе \_ (MF)**](mf-toponode-workqueue-mmcss-class-attribute.md)

Если приложение регистрирует один из собственных потоков с помощью MMCSS, можно использовать этот атрибут, чтобы связать рабочую очередь топологии с группой MMCSS приложения. Задайте значение атрибута, равное идентификатору задачи, полученному приложением при регистрации в службе MMCSS. (Идентификатор задачи возвращается в параметре *таскиндекс* функции [**авсетммсреадчарактеристикс**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) . Дополнительные сведения см. в разделе [процесс и функции потока](../procthread/process-and-thread-functions.md).

Если вы хотите, чтобы служба MMCSS назначила новый идентификатор задачи для топологии, установите [**атрибут \_ \_ \_ \_ класса MMCSS топоноде ворккуеуе (MF**](mf-toponode-workqueue-mmcss-class-attribute.md) ), но не задавайте атрибут **MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID** .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> <dt>

[Рабочие очереди](work-queues.md)
</dt> </dl>

 

 
