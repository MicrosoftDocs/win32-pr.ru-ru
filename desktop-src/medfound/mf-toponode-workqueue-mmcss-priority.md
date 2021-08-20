---
description: Задает относительный приоритет потока для ветви топологии.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1b131e6c8b0f379e5e7951498c52f7c0d7a3eab83b75fed4ab9e8100721668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874797"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>\_ \_ \_ \_ Атрибут приоритета MMCSS топоноде ворккуеуе MF

Задает относительный приоритет потока для ветви топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**). Атрибут является необязательным.

Для этого атрибута требуются атрибуты класса [MF \_ топоноде \_ Ворккуеуе \_ ID](mf-toponode-workqueue-id-attribute.md) и [MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) на одном узле.

Значение атрибута — это относительный приоритет потока рабочей очереди для этой ветви топологии. [Служба диспетчера классов мультимедиа](../procthread/multimedia-class-scheduler-service.md) (MMCSS) использует относительный приоритет, если он задает приоритет потока. Дополнительные сведения см. в разделе [**авсетммсреадприорити**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 
