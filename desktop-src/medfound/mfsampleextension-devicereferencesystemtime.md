---
description: Задает исходную метку времени устройства для образца.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Атрибут MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0458c1a2b0f5b204483cba0e6f571a2a5ace34b7b39463cc20ded664eecaaa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241139"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>Мфсампликстенсион \_ девицереференцесистемтиме, атрибут

Задает исходную метку времени устройства для образца.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Remarks

Это метка времени ссылки на устройство примеры носителей в разрешении 100 нс. Эта отметка времени может не содержать фактическое значение счетчика производительности запросов (QPC) в зависимости от источника, производящего выборки. Это значение может быть изменено другими компонентами в конвейере мультимедиа. Это значение недоступно для МФТС, вставленного в конвейер захвата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




