---
description: Указывает идентификатор ключа для зашифрованного файла расширенных систем формата (ASF). Этот атрибут соответствует полю Идентификатор ключа в заголовке шифрования содержимого, определенном в спецификации ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: Атрибут MF_PD_ASF_CONTENTENCRYPTION_KEYID (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144782"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>\_ \_ \_ \_ Атрибут контентенкриптион KEYID для MF PD ASF

Указывает идентификатор ключа для зашифрованного файла расширенных систем формата (ASF). Этот атрибут соответствует полю Идентификатор ключа в заголовке шифрования содержимого, определенном в спецификации ASF.

## <a name="data-type"></a>Тип данных

Строка расширенных символов

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к дескрипторам представления для содержимого ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) ИЗВЛЕКАЕТ поле идентификатора ключа, преобразует его в строку расширенных символов, а затем заполняет массив типа **WCHAR** с завершающим нулем. Размер массива равен значению поля Длина идентификатора ключа в заголовке шифрования содержимого.

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

[**Имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> <dt>

[Объект заголовка ASF](asf-file-structure.md)
</dt> <dt>

[Дескрипторы представления](presentation-descriptors.md)
</dt> </dl>

 

 




