---
description: Содержит данные шифрования для файла ASF. Этот атрибут соответствует объекту расширенного шифрования содержимого в заголовке ASF, определенном в спецификации ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: Атрибут MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f6be55339d61a22dc98737c56213a5fdbe4e1eb7f881f7ba1c4d6b5a5ab7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059672"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a>\_ \_ \_ \_ Атрибут данных шифрования MF PD ASF контентенкриптионекс \_

Содержит данные шифрования для файла ASF. Этот атрибут соответствует объекту расширенного шифрования содержимого в заголовке ASF, определенном в спецификации ASF.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Этот атрибут применяется к дескрипторам представления для содержимого ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из заголовка объекта расширенного шифрования содержимого. Размер большого двоичного объекта равен полю размера данных. Массив байтов, содержащийся в большом двоичном объекте, совпадает с полем данных в расширенном наборе шифрования содержимого заголовка ASF.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 




