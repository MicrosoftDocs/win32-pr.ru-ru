---
description: Хранит указатель IUnknown класса, реализующего интерфейс Имфсслцертификатеманажер.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Свойство MFNETSOURCE_SSLCERTIFICATE_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f853ae3fe44a9c4508386df4096e4adac36f3cec8a8cf199eb91cb87e1fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243298"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>МФНЕТСАУРЦЕ \_ сслцертификате \_ Manager, свойство

Хранит указатель **IUnknown** класса, реализующего интерфейс [**имфсслцертификатеманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) . Реализация клиента предоставляет методы для получения SSL-сертификата клиента, когда он запрашивается сервером.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**Указатель IUnknown**

VT \_ Unknown

**пунквал**



## <a name="remarks"></a>Remarks

Константа **мфнетсаурце \_ сслцертификате \_ Manager** определяет идентификатор GUID для ключа свойства. Идентификатор свойства (PID) равен нулю. Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




