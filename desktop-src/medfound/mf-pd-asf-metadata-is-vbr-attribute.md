---
description: Указывает, использует ли файл в расширенном системном формате (ASF) кодирование с переменной скоростью (VBR).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: Атрибут MF_PD_ASF_METADATA_IS_VBR (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683874"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a>MF \_ PD \_ \_ метаданные ASF \_ — \_ атрибут VBR

Указывает, использует ли файл в расширенном системном формате (ASF) кодирование с переменной скоростью (VBR).

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к дескрипторам представления для содержимого ASF. Если значение равно **true**, файл был закодирован с помощью VBR. Если значение равно **false** или отсутствует атрибут, файл не использует кодирование VBR.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут и задает его в дескрипторе представления.

> [!Note]  
> Этот атрибут соответствует атрибуту **исвбр** в пакете SDK формата Windows Media.

 

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

 

 




