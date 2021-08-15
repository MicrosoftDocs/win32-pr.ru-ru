---
description: Указывает идентификатор задачи службы планировщика классов мультимедиа (MMCSS) для ветви топологии.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf75dc911c9d00cab2d21d937ef16a43b38cc4271299c6fae4f2ed7381ec63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739632"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>\_Атрибут MF топоноде \_ ворккуеуе \_ MMCSS \_

Указывает идентификатор задачи службы планировщика классов мультимедиа (MMCSS) для ветви топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**). Этот атрибут является необязательным.

Этот атрибут игнорируется, если не заданы также следующие атрибуты:

-   [**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**](mf-toponode-workqueue-id-attribute.md)
-   [**\_ \_ \_ класс MMCSS ТОПОНОДЕ ворккуеуе \_ (MF)**](mf-toponode-workqueue-mmcss-class-attribute.md)

Если приложение регистрирует один из собственных потоков с помощью MMCSS, можно использовать этот атрибут, чтобы связать рабочую очередь топологии с группой MMCSS приложения. Задайте значение атрибута, равное идентификатору задачи, полученному приложением при регистрации в службе MMCSS. (Идентификатор задачи возвращается в параметре *таскиндекс* функции [**авсетммсреадчарактеристикс**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) . Дополнительные сведения см. в разделе [процесс и функции потока](../procthread/process-and-thread-functions.md).

Если вы хотите, чтобы служба MMCSS назначила новый идентификатор задачи для топологии, установите [**атрибут \_ \_ \_ \_ класса MMCSS топоноде ворккуеуе (MF**](mf-toponode-workqueue-mmcss-class-attribute.md) ), но не задавайте атрибут **MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID** .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
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

 

 
