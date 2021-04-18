---
description: Указывает максимальную скорость передачи данных (в битах в секунду) для потока в файле расширенных систем формата (ASF).
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: Атрибут MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85626be11afe2e9413852e8aec3533f987538473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712709"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a>Атрибут скорости MF \_ SD \_ ASF \_ екстстрмпроп, \_ максимальный \_ скорость передачи данных \_

Указывает максимальную скорость передачи данных (в битах в секунду) для потока в файле расширенных систем формата (ASF).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к дескрипторам потоков для содержимого ASF. Он соответствует полю Альтернативная скорость битов данных в объекте свойств расширенного потока. Дополнительные сведения см. в спецификации ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF. Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

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

[**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Атрибуты дескриптора потока](stream-descriptor-attributes.md)
</dt> <dt>

[Объект заголовка ASF](asf-file-structure.md)
</dt> </dl>

 

 




