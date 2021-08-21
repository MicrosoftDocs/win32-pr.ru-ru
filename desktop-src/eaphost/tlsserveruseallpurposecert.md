---
title: тлссерверусеаллпурпосецерт
description: Раздел реестра Тлссерверусеаллпурпосецерт определяет, используются ли для проверки подлинности EAP-TLS сертификаты всех целей.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2f9d47b4e80409c27c71fe3655a1d3266571e0f8a8dd757e5334b0ef9fec40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085699"
---
# <a name="tlsserveruseallpurposecert"></a>тлссерверусеаллпурпосецерт

Раздел реестра Тлссерверусеаллпурпосецерт определяет, используются ли для проверки подлинности EAP-TLS сертификаты всех целей.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ DWORD** .



| Значение        | Описание                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Для проверки подлинности PEAP выбираются сертификаты всех целей в хранилище сертификатов клиента или сервера.     |
| Другие значения | Сертификаты всех целей в хранилище сертификатов клиента или сервера не выбраны для проверки подлинности PEAP. |



 

Если это значение реестра отсутствует, для проверки подлинности EAP-TLS выбираются сертификаты всех целей в хранилище сертификатов клиента или сервера.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Параметры реестра EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




