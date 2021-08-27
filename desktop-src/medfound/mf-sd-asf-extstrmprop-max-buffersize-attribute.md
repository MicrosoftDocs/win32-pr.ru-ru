---
description: Указывает максимальный размер буфера в байтах, необходимый для потока в файле ASF.
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: Атрибут MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399f6af425020a72caf6185da18f7747c037a71245b8e8d841d886d7b7eabd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113734"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a>MF \_ SD \_ ASF \_ екстстрмпроп \_ Max, \_ атрибут BUFFERSIZE

Указывает максимальный размер буфера в байтах, необходимый для потока в файле ASF.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к дескрипторам потоков для содержимого ASF. Он соответствует полю "Размер альтернативного буфера" в объекте свойств расширенного потока. Дополнительные сведения см. в спецификации ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF. Приложение может создать дескриптор потока для потока из дескриптора представления путем вызова [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 




