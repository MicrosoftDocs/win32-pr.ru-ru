---
description: Указывает профиль соответствия устройства для кодирования файлов формата ASF.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Атрибут MF_TRANSCODE_ENCODINGPROFILE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543234"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>\_Атрибут енкодингпрофиле для ПЕРЕКОДИРОВАНИЯ MF \_

Указывает профиль соответствия устройства для кодирования файлов формата ASF.

## <a name="data-type"></a>Тип данных

**LPWSTR**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: жеталлокатедстринг**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Комментарии

Используйте этот атрибут при перекодировании на устройство, которое поддерживает Windows Media. Если этот атрибут задан, кодировщик будет использовать профиль согласования устройства или шаблон для кодеков Windows Media. Перед созданием топологии перекодировки задайте атрибут в профиле перекодировки.

Значением этого атрибута может быть любая из строк шаблона соответствия, перечисленных в следующих разделах:

-   [Шаблоны соответствия аудио устройства](../wmformat/audio-device-conformance-templates.md)
-   [Шаблоны соответствия видеоустройств](../wmformat/video-device-conformance-templates.md)

Для кодирования видео Windows Media построитель топологии использует этот атрибут для задания свойства [**мфпкэй \_ декодеркомплекситирекуестед**](mfpkey-decodercomplexityrequestedproperty.md) в кодировщике. Кодировщик будет пытаться использовать указанный шаблон для кодирования содержимого. Чтобы получить фактический шаблон, проведите обход узлов топологии перекодировки, чтобы получить указатель на узел кодировщика. Затем получите значение свойства [**мфпкэй \_ декодеркомплекситипрофиле**](mfpkey-decodercomplexityprofileproperty.md) из кодировщика.

Построитель топологии также использует значение этого атрибута для задания свойства "Девицеконформанцетемплате" в приемнике ASF Media.

Если этот атрибут задан, то объект метаданных ASF-файла всегда создается независимо от значения, указанного приложением, для атрибута [ \_ \_ \_ \_ пересылки метаданных пропуска MF](mf-transcode-skip-metadata-transfer.md) .

Ниже приведены типичные значения для этого атрибута.



| Значение   | Описание                      |
|---------|----------------------------------|
| ПРОФИЛЯ    | Видео расширенного профиля           |
| МВ    | Видео о основном профиле               |
| ПОРТОВ    | Видео простого профиля             |
| "MP@LL" | Основной профиль, видео среднего уровня |
| L2    | Профиль аудиоподсистемы, <= 160 кбит/с    |



 

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

[API перекодирования](transcode-api.md)
</dt> <dt>

[**Имфтранскодепрофиле:: Жетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**Имфтранскодепрофиле:: Сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**Имфтранскодепрофиле:: Сетвидеоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**Имфтранскодепрофиле:: Жетвидеоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
