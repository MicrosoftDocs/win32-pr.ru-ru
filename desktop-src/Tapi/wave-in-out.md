---
description: Класс устройства "звук/вход/выход" состоит из полных звуковых устройств.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: звук/вход/выход
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f526caf461cbf0bb5c3fb5490cf5e9141d9735e37e10ab632749006135a1cc9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860413"
---
# <a name="waveinout"></a>звук/вход/выход

Класс устройства "звук/вход/выход" состоит из полных звуковых устройств. Доступ к этим устройствам осуществляется с помощью функций Wave, которые описаны в пакете SDK для платформы. Устройства в этом классе связаны с линейными устройствами, поддерживающими \_ тип носителя линемедиамоде аутоматедвоице, который указан в **двмедиамодес** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для линейного устройства.

Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя два дополнительных члена:

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

Члены **девицеинид** и **девицеаутид** являются идентификаторами закрытого звукового устройства. Эти идентификаторы используются в вызове функции [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) для открытия устройства для вывода. Полученный в результате маркер устройства можно использовать для воспроизведения цифровых звуковых данных на устройстве Line или Phone.

Дополнительные сведения о функциях Wave см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).

 

 
