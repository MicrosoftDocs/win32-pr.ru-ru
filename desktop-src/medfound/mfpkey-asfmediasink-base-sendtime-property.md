---
description: Базовое время отправки для приемника мультимедиа ASF в миллисекундах.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: Свойство MFPKEY_ASFMEDIASINK_BASE_SENDTIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693879"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a>МФПКЭЙ \_ асфмедиасинк \_ базовое \_ свойство сендтиме

Базовое время отправки для приемника мультимедиа ASF в миллисекундах.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**ULONG**

VT \_ UI4

**улвал**



## <a name="remarks"></a>Комментарии

Время отправки — это время, когда пакет ASF отправляется по сети. Он не соответствует непосредственно времени презентации данных в пакете.

Это свойство можно использовать для настройки приемника мультимедиа ASF. Использование зависит от того, какая функция вызывается для создания приемника мультимедиа ASF:

-   [**Мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): запросите полученный указатель [**Имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) для интерфейса **ипропертисторе** .

-   [**Мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): вызов [**Имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) в указателе [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , указанном в параметре *pContentInfo* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




