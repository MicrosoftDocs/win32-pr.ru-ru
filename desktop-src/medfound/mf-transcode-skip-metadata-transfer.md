---
description: Указывает, записываются ли метаданные в перекодированный файл.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Атрибут MF_TRANSCODE_SKIP_METADATA_TRANSFER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7874d7d8cc20bbf5222cd8fd2fa0ca938c0b597dbc42914ab809dad926968306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739426"
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

## <a name="remarks"></a>Remarks

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфтранскодепрофиле:: Жетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**Имфтранскодепрофиле:: Сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




