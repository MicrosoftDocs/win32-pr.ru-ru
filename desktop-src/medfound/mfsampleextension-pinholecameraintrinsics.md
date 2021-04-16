---
description: Содержит встроенные функции камеры пинхоле для образца.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: Атрибут MFSampleExtension_PinholeCameraIntrinsics (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719469"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a>Мфсампликстенсион \_ пинхолекамераинтринсикс, атрибут

Содержит встроенные функции камеры пинхоле для образца.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Комментарии

Значением атрибута является [**мфпинхолекамераинтринсикс**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

Этот атрибут является необязательным для поддержки камер, которые не были откалиброваны.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                        |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



 

 




