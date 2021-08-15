---
title: пеапсерверакцепталлпурпосецерт
description: Раздел реестра Пеапсерверакцепталлпурпосецерт определяет, принимаются ли сертификаты всех целей для проверки подлинности PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d568ef2cf3e7fd5eeeaa650e5e6e4fd32a8e1c8d6baa0ed91434a5c0aa60ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784686"
---
# <a name="peapserveracceptallpurposecert"></a>пеапсерверакцепталлпурпосецерт

Раздел реестра Пеапсерверакцепталлпурпосецерт определяет, принимаются ли сертификаты всех целей для проверки подлинности PEAP.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ DWORD** .



| Значение        | Описание                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Сервер и клиент принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности EAP-TLS.       |
| Другие значения | Сервер и клиент не принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности EAP-TLS |



 

Если этот параметр реестра отсутствует, сервер и клиент принимают сертификаты всех целей, отправленные другой стороной для проверки подлинности PEAP.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Параметры реестра EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




