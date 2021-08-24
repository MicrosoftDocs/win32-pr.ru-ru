---
description: Содержит внешние видеокамеры для образца.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: Атрибут MFSampleExtension_CameraExtrinsics (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109dd0d171468d3a0a3c2c4f06ba1a7edc18707aa1e17afe0d1be65509f4266d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722664"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a>Мфсампликстенсион \_ камераекстринсикс, атрибут

Содержит внешние видеокамеры для образца.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

Значением атрибута является [**мфкамераекстринсикс**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

Этот атрибут является необязательным для поддержки камер, которые не были откалиброваны.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




