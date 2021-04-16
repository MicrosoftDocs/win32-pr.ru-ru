---
description: Следующие идентификаторы GUID определяют расширения полезных данных для потоков ASF.
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: Идентификаторы GUID расширения полезных данных ASF (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539650"
---
# <a name="asf-payload-extension-guids"></a>Идентификаторы GUID расширения полезных данных ASF

Следующие идентификаторы GUID определяют расширения полезных данных для потоков ASF.



| Константа                                                                                                                                                                                                                                                                                      | Описание                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**Мфасфсампликстенсион \_ сампледуратион**</dt> </dl>         | Данные указывают длительность (в миллисекундах) образца, содержащегося в объекте buffer.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**Мфасфсампликстенсион \_ аутпутклеанпоинт**</dt> </dl> | Данные указывают, является ли образец ключевым кадром. Нулевое значение указывает, что образец не является ключевым кадром. Ненулевое значение указывает, что это ключевой кадр.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**Мфасфсампликстенсион \_ SMPTE**</dt> </dl>                                             | Данные представляют собой код времени SMPTE.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**\_Имя файла мфасфсампликстенсион**</dt> </dl>                                 | Данные в примере расширения указывают имя файла, из которого было получено содержимое в образце.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**\_ContentType мфасфсампликстенсион**</dt> </dl>                     | Данные определяют тип содержимого, которое содержит образец.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**Мфасфсампликстенсион \_ пикселаспектратио**</dt> </dl> | Данные обозначают пропорцию содержимого в образце пикселя.<br/>                                                                                               |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имфасфстреамконфиг:: Аддпайлоадекстенсион**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**Имфасфстреамконфиг:: Жетпайлоадекстенсион**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Константы Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




