---
description: Указывает время в 100-наносекундных единицах, необходимое для отправки файла ASF. Время отправки пакетов — это время, когда пакет должен быть доставлен по сети. Это не время презентации пакета.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: Атрибут MF_PD_ASF_FILEPROPERTIES_SEND_DURATION (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce635cd02766a3c9ca8b0a0d327db93a4bcaaca76bccd6ae54fda726684ec641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740946"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a>\_ \_ \_ \_ \_ Атрибут длительности отправки для MF PD ASF филепропертиес

Указывает время в 100-наносекундных единицах, необходимое для отправки файла ASF. *Время отправки* пакета — это время, когда пакет должен быть доставлен по сети. Это не время презентации пакета.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к дескрипторам представления для содержимого ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> <dt>

[Объект заголовка ASF](asf-file-structure.md)
</dt> <dt>

[Дескрипторы представления](presentation-descriptors.md)
</dt> </dl>

 

 




