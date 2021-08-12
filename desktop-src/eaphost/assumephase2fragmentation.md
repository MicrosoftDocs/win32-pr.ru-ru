---
title: AssumePhase2Fragmentation
description: Раздел реестра AssumePhase2Fragmentation определяет, предполагает ли сервер и клиент фрагментацию этапа 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caee785b0c89b92aaf4b01c590425c451b9a977664e915874e7eb5ad1edf46aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275841"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

Раздел реестра AssumePhase2Fragmentation определяет, предполагает ли сервер и клиент фрагментацию этапа 2.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ DWORD** .



| Значение   | Описание                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | Сервер и клиент предполагают, что другая сторона не поддерживает 2 этапа фрагментации во время аутентификации PEAP. |
| отличные | Сервер и клиент предполагают, что другая сторона поддерживает этап 2 во время проверки подлинности PEAP.     |



 

Если это значение реестра отсутствует, сервер и клиент предполагают, что другая сторона поддерживает фрагментацию второго этапа во время аутентификации PEAP.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Параметры реестра EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




