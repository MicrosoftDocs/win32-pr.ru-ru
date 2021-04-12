---
description: Указывает, записываются ли метаданные в перекодированный файл.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Атрибут MF_TRANSCODE_SKIP_METADATA_TRANSFER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263358"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>\_Перекодировать \_ атрибут пропуска \_ метаданных \_

Указывает, записываются ли метаданные в перекодированный файл. Этот атрибут контейнера хранится в профиле перекодирования.

## <a name="data-type"></a>Тип данных

**UINT32**

\_ \_ В следующей таблице описаны возможные значения атрибута, пропуская \_ \_ Перенаправление метаданных MF.



| Значение                                                                        | Значение                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Автоматически передает метаданные на уровне файлов из исходного файла в перекодированный файл.<br/> |
| <dl> <dt>1</dt> </dl> | Метаданные исходного файла не записываются в перекодированный файл.<br/>                          |



 

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфтранскодепрофиле:: Жетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**Имфтранскодепрофиле:: Сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




