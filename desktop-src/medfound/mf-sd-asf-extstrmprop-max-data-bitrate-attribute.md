---
description: Указывает максимальную скорость передачи данных (в битах в секунду) для потока в файле расширенных систем формата (ASF).
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: Атрибут MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9bb445724c15604ab30e353315769f78a71c0d6dd94291392e4c34ee05a70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714364"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a>Атрибут скорости MF \_ SD \_ ASF \_ екстстрмпроп, \_ максимальный \_ скорость передачи данных \_

Указывает максимальную скорость передачи данных (в битах в секунду) для потока в файле расширенных систем формата (ASF).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к дескрипторам потоков для содержимого ASF. Он соответствует полю Альтернативная скорость битов данных в объекте свойств расширенного потока. Дополнительные сведения см. в спецификации ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF. Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Атрибуты дескриптора потока](stream-descriptor-attributes.md)
</dt> <dt>

[Объект заголовка ASF](asf-file-structure.md)
</dt> </dl>

 

 




