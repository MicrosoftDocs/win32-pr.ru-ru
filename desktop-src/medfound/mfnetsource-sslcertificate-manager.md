---
description: Хранит указатель IUnknown класса, реализующего интерфейс Имфсслцертификатеманажер.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Свойство MFNETSOURCE_SSLCERTIFICATE_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710811"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>МФНЕТСАУРЦЕ \_ сслцертификате \_ Manager, свойство

Хранит указатель **IUnknown** класса, реализующего интерфейс [**имфсслцертификатеманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) . Реализация клиента предоставляет методы для получения SSL-сертификата клиента, когда он запрашивается сервером.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**Указатель IUnknown**

VT \_ Unknown

**пунквал**



## <a name="remarks"></a>Комментарии

Константа **мфнетсаурце \_ сслцертификате \_ Manager** определяет идентификатор GUID для ключа свойства. Идентификатор свойства (PID) равен нулю. Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




