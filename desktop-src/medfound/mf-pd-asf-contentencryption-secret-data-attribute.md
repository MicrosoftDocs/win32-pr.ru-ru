---
description: Содержит секретные данные для зашифрованного файла расширенных систем (ASF). Этот атрибут соответствует полю данных секрета в заголовке шифрования содержимого, определенном в спецификации ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: Атрибут MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541359"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a>\_ \_ \_ \_ Атрибут данных секрета MF PD ASF контентенкриптион \_

Содержит секретные данные для зашифрованного файла расширенных систем (ASF). Этот атрибут соответствует полю данных секрета в заголовке шифрования содержимого, определенном в спецификации ASF.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к дескрипторам представления для содержимого ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) заполняет массив байтов полем секретных данных. Размер массива равен значению поля "Секретная длина данных" заголовка шифрования содержимого.

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

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> <dt>

[Объект заголовка ASF](asf-file-structure.md)
</dt> <dt>

[Дескрипторы представления](presentation-descriptors.md)
</dt> </dl>

 

 




