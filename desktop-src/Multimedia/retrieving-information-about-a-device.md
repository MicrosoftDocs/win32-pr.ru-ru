---
title: Получение сведений об устройстве
description: Получение сведений об устройстве
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- Команда MCI_GETDEVCAPS
- Команда MCI_STATUS
- Команда MCI_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412ccfb8819ac1c76cd3f0114fa114c877280de959f605535fd4bb83d224a91e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689094"
---
# <a name="retrieving-information-about-a-device"></a>Получение сведений об устройстве

Каждое устройство реагирует на [**возможности**](capability.md) ([**MCI \_ жетдевкапс**](mci-getdevcaps.md)), [**состояние**](status.md) ([**\_ состояние MCI**](mci-status.md)) и [**сведения**](info.md) ([**\_ сведения о MCI**](mci-info.md)). Эти команды получают сведения об устройстве. Например, следующая команда возвращает значение true, если устройство **кдаудио** может извлечь диск:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Флаги, перечисленные для обязательных и основных команд, предоставляют минимальный объем сведений об устройстве. Многие устройства дополняют необходимые и базовые команды с расширенными флагами для предоставления дополнительных сведений об устройстве.

 

 




