---
description: Содержит встроенные функции камеры пинхоле для образца.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: Атрибут MFSampleExtension_PinholeCameraIntrinsics (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb26cd7931b1dfe2e17dcd1b8dfff8ee7f972f6dad066bee6879f0de12b3609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113084"
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

## <a name="remarks"></a>Remarks

Значением атрибута является [**мфпинхолекамераинтринсикс**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

Этот атрибут является необязательным для поддержки камер, которые не были откалиброваны.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



 

 




