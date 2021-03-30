---
description: Содержит указатель на хранилище свойств со свойствами кодировки.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Атрибут MF_SINK_WRITER_ENCODER_CONFIG (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814889"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>\_ \_ \_ Атрибут конфигурации кодировщика записи MF SINK \_

Содержит указатель на хранилище свойств со свойствами кодировки.

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Значением этого атрибута является указатель [_ *ипропертисторе* *](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Этот атрибут позволяет приложению задавать свойства кодировки при использовании [модуля записи приемника](sink-writer.md). Чтобы задать этот атрибут, выполните следующие действия.

1.  Вызовите [**пскреатемеморипропертисторе**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) , чтобы создать новое хранилище свойств.
2.  Задайте свойства кодировщика в хранилище свойств. Доступные свойства зависят от кодировщика. Дополнительные сведения см. в разделе [объекты кодека](codecobjects.md).
3.  Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов.
4.  Вызовите метод [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) , чтобы задать указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в хранилище атрибутов.
5.  Создайте новый экземпляр модуля записи приемника. Передайте указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) функции создания. Дополнительные сведения см. в разделе [атрибуты модуля записи приемника](sink-writer-attributes.md).

Модуль записи приемника задает свойства кодировщика перед заданием типов мультимедиа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**имфсинквритер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Атрибуты модуля записи приемника](sink-writer-attributes.md)
</dt> </dl>

 

 
