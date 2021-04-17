---
description: Класс устройства "звук/вход/выход" состоит из полных звуковых устройств.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: звук/вход/выход
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673961"
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

 

 
