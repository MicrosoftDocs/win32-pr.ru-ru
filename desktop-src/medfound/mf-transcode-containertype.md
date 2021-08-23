---
description: Указывает тип контейнера закодированного файла.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: Атрибут MF_TRANSCODE_CONTAINERTYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c56b0332c43f10fa61b34f47191e3946a4813b3670249a8d858317067c38d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604694"
---
# <a name="mf_transcode_containertype-attribute"></a>\_Атрибут контаинертипе для ПЕРЕКОДИРОВАНИЯ MF \_

Указывает тип контейнера закодированного файла. Типы контейнеров поддерживаются Media Foundation.

## <a name="data-type"></a>Тип данных

**GUID**

Возможные значения для типов контейнеров, предоставляемых Media Foundation, описаны в следующей таблице.



| Значение                                                                                                                                                                                                                                                                 | Значение                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ ASF**</dt> </dl>             | Контейнер файлов ASF.<br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ MPEG4**</dt> </dl>     | Контейнер файла MP4.<br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ MP3**</dt> </dl>             | Контейнер файлов MP3.<br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ 3GP**</dt> </dl>             | контейнер файлов 3GP. <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ AC3**</dt> </dl>             | Контейнер файлов AC3. <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ ADTS**</dt> </dl>         | Контейнер файлов ADTS. <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ MPEG2**</dt> </dl>     | Контейнер файлов MPEG2. <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ FMPEG4**</dt> </dl> | Контейнер файлов FMPEG4. <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <dt>**\_Волна мфтранскодеконтаинертипе**</dt> </dl>         | Контейнер файла WAVE.<br/> поддерживается в Windows 8.1 и более поздних версиях.<br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ AVI**</dt> </dl>             | Контейнер файла AVI.<br/> поддерживается в Windows 8.1 и более поздних версиях.<br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <dt>**Мфтранскодеконтаинертипе \_ AMR**</dt> </dl>             | Контейнер файлов AMR. <br/>                                                    |



 

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Remarks

Этот атрибут используется как для функции быстрого перекодирования, так и для объекта модуля записи приемника.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

### <a name="fast-transcode"></a>Быстрый перекодированный

Перед сборкой топологии перекодировки приложение должно установить атрибут контейнера в профиле перекодировки. Построитель топологии анализирует этот атрибут и загружает в конвейере соответствующий приемник мультимедиа. Дополнительные сведения см. в следующих разделах:

-   [**Имфтранскодепрофиле:: Жетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [**Имфтранскодепрофиле:: Сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a>Модуль записи приемников

Этот атрибут можно использовать для настройки типа контейнера файлов для модуля записи приемника. Дополнительные сведения см. в разделе [атрибуты модуля записи приемника](sink-writer-attributes.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API перекодирования](transcode-api.md)
</dt> </dl>

 

 




