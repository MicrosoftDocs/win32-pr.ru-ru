---
description: Указывает рабочую очередь для ветви топологии.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: Атрибут MF_TOPONODE_WORKQUEUE_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154983"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>\_ \_ Атрибут ID ТОПОНОДЕ ворккуеуе MF \_

Указывает рабочую очередь для ветви топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**). Атрибут является необязательным.

Значение атрибута является определяемым приложением идентификатором для рабочей очереди.

Приложения могут использовать этот атрибут для назначения рабочих очередей ветвей топологии. Каждый исходный узел в топологии определяет одну ветвь. Ветвь включает все узлы топологии, которые получают данные из этого узла.

Если этот атрибут задан, вызовите метод [**имфворккуеуесервицес:: бегинрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) для разрешенной топологии. Несколько ветвей в топологии могут совместно использовать одну и ту же рабочую очередь, а рабочие очереди можно повторно использовать в топологиях.

> [!Note]  
> Значение этого атрибута не совпадает с идентификатором, возвращаемым функцией [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) . Значение атрибута является определяемым приложением идентификатором и используется для связи ветвей топологии с рабочими очередями. Когда сеанс мультимедиа выделяет новую рабочую очередь, он сохраняет фактический идентификатор рабочей очереди внутри.

 

Если этот атрибут задан, приложение также может назначить ветвь для задачи службы планировщика классов мультимедиа, задав атрибут [**\_ \_ \_ \_ класса топоноде ворккуеуе MMCSS**](mf-toponode-workqueue-mmcss-class-attribute.md) .

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

[**\_ \_ \_ класс MMCSS ТОПОНОДЕ ворккуеуе \_ (MF)**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> <dt>

[Рабочие очереди](work-queues.md)
</dt> </dl>

 

 




