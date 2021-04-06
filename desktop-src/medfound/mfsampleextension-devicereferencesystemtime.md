---
description: Задает исходную метку времени устройства для образца.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Атрибут MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898194"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>Мфсампликстенсион \_ девицереференцесистемтиме, атрибут

Задает исходную метку времени устройства для образца.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Комментарии

Это метка времени ссылки на устройство примеры носителей в разрешении 100 нс. Эта отметка времени может не содержать фактическое значение счетчика производительности запросов (QPC) в зависимости от источника, производящего выборки. Это значение может быть изменено другими компонентами в конвейере мультимедиа. Это значение недоступно для МФТС, вставленного в конвейер захвата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                   |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




