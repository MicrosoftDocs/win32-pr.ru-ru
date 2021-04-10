---
description: Задает режим обработки Стабилизация видео MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Атрибут MF_VIDEODSP_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154974"
---
# <a name="mf_videodsp_mode-attribute"></a>\_ \_ Атрибут режима видеодсп MF

Задает режим обработки [**стабилизация видео MFT**](video-stabilization-mft.md).

## <a name="data-type"></a>Тип данных

**Мфвидеодспмоде** хранится в виде **UIINT32**

## <a name="remarks"></a>Комментарии

Значением этого атрибута является значение перечисления [**мфвидеодспмоде**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Этот атрибут можно использовать для включения или отключения образа стабилизации и может быть обновлен для каждого образца выходных данных.

Чтобы задать этот атрибут, сделайте следующее:

1.  Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в файле MFT видео стабилизации, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Вызовите метод [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы задать атрибут.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Стабилизация видео MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




