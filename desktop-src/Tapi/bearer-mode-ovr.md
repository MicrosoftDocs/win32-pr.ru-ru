---
description: Режим носителя соответствует качеству передачи, запрошенному из сети для установления вызова.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Режим носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263836"
---
# <a name="bearer-mode"></a>Режим носителя

[**Режим носителя**](./linebearermode--constants.md) соответствует качеству передачи, запрошенному из сети для установления вызова. Важно помнить, что понятие режима носителя не отличается от [**типа носителя**](tapimediatype--constants.md). Например, аналоговая телефонная сеть (PSTN) обеспечивает только режим носителя в 3,1 кГц, но вызов с его помощью может поддерживать такие типы носителей, как голосовой, Факс или модем данных.

Режим носителя вызова указывается, когда вызов настраивается или предоставляется при вызове метода. Если линейные устройства могут представлять пулы каналов, поставщик услуг может разрешить вызовы с более широкой пропускной способностью.

Не все поставщики служб поддерживают использование этих сведений.

**Интерфейс TAPI 2. x:** См. раздел [**линесеткаллпарамс**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двбеарермоде** член [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**иткаллинфо::p UT \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ беарермоде** [**каллинфо \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

**Тспи:** См. [**строку \_ каллинфо**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) Message, где для *DWPARAM1* задано значение линекаллинфостате \_ беарермоде.

 

 
