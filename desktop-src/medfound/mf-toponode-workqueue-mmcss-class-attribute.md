---
description: Указывает задачу службы планировщика классов мультимедиа (MMCSS) для ветви топологии.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: Атрибут MF_TOPONODE_WORKQUEUE_MMCSS_CLASS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6630cf22d3afe270b2a032304fd9de3118e73e75e28da4116418894271237a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739848"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a>\_ \_ \_ Атрибут класса MMCSS топоноде ворккуеуе MF \_

Указывает задачу [службы планировщика классов мультимедиа](../procthread/multimedia-class-scheduler-service.md) (MMCSS) для ветви топологии.

## <a name="data-type"></a>Тип данных

Строка расширенных символов

## <a name="remarks"></a>Remarks

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**). Этот атрибут является необязательным.

Для этого атрибута требуется [атрибут \_ \_ \_ ID MF топоноде ворккуеуе](mf-toponode-workqueue-id-attribute.md) . Если задан этот атрибут, также необходимо установить атрибут **\_ \_ \_ идентификатора MF топоноде ворккуеуе** на том же узле.

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

[**Имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ \_ ИД ворккуеуе ТОПОНОДЕ для MF \_**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ топоноде \_ ворккуеуе \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> <dt>

[Рабочие очереди](work-queues.md)
</dt> </dl>

 

 
