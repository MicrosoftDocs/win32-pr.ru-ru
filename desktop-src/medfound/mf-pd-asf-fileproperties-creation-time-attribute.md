---
description: Указывает дату и время создания файла расширенных систем форматирования (ASF).
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: Атрибут MF_PD_ASF_FILEPROPERTIES_CREATION_TIME (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1a015e251e04c706e2d36b7ab85cac4e8038ad2083c9e0089fbe847d835227a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104360"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a>\_ \_ \_ \_ Атрибут времени создания MF PD ASF филепропертиес \_

Указывает дату и время создания файла расширенных систем форматирования (ASF).

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Этот атрибут применяется к дескрипторам представления для содержимого ASF. значением атрибута является структура **FILETIME** , которая описана в Windows SDK.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает этот атрибут из метаданных ASF.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
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

 

 




