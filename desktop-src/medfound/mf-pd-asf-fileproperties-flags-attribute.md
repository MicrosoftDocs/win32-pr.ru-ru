---
description: Указывает, является ли файл ASF-файла широковещательным или недоступным для поиска. Это значение соответствует полю flags объекта свойств файла, определенному в спецификации ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Атрибут MF_PD_ASF_FILEPROPERTIES_FLAGS (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656644"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>\_ \_ \_ \_ Атрибут флагов филепропертиес MF для ASF

Указывает, является ли файл ASF-файла широковещательным или недоступным для поиска. Это значение соответствует полю flags объекта свойств файла, определенному в спецификации ASF.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к дескрипторам представления для содержимого ASF. Значение атрибута является побитовым оператором или для следующих флагов:



| Flag | Описание                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | Флаг вещания. Файл находится в процессе создания.                                                                                                                                                                                                                                      |
| 0x02 | Флаг с возможностью поиска. Файл доступен для поиска.<br/> Файл доступен для поиска, если имеется звуковой поток, а максимальный размер пакета данных равен минимальному размеру пакета данных. Он также может быть доступен для поиска, если файл содержит аудиопоток и видеопоток с соответствующим простым объектом index.<br/> |



 

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.

Если установлен флаг вещания, следующие атрибуты в дескрипторе представления недопустимы:

-   [**MF \_ PD \_ ASF \_ филепропертиес \_ File \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**\_ \_ \_ \_ время создания филепропертиес MF PD \_ ASF**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**\_пакеты MF PD \_ ASF \_ филепропертиес \_**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**\_ \_ \_ длительность воспроизведения MF филепропертиес \_ ASF \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**\_период отправки MF PD \_ ASF \_ филепропертиес \_ \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)

Кроме того, в атрибуте [**\_ \_ \_ Филепропертиес \_ максимального \_ \_ размера пакета MF**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) и MF, ASF, [**\_ \_ \_ филепропертиес \_ min \_ \_ PD**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) , в качестве значений атрибутов устанавливается фактический размер пакета.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
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

 

 




