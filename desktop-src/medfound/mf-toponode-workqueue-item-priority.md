---
description: Указывает приоритет рабочего элемента для ветви топологии.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Атрибут MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff67e48bda6ac00baeab9418b80d366c23808713b4689a013949b364f09b6e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739838"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>\_ \_ \_ Атрибут приоритета элемента MF топоноде ворккуеуе \_

Указывает приоритет рабочего элемента для ветви топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к исходным узлам **( \_ \_ \_ узел топологии MF саурцестреам**). Атрибут является необязательным.

Для этого атрибута требуется [атрибут \_ \_ \_ ID MF топоноде ворккуеуе](mf-toponode-workqueue-id-attribute.md) на том же узле.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                               |
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
</dt> </dl>

 

 




