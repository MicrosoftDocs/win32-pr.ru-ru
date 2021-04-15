---
description: После назначения адреса TAPI назначает идентификаторы адресов.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Идентификаторы адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682541"
---
# <a name="address-identifiers"></a>Идентификаторы адресов

После назначения адреса TAPI назначает идентификаторы адресов. *Идентификатор адреса* — это число от 0 до количества адресов в строке минус единица. Идентификатор адреса — это постоянное число, назначенное данному устройству, и остается постоянным даже при обновлении операционной системы. Сочетание [идентификатора устройства](device-identifier-ovr.md) и идентификатора адреса однозначно определяет заданный адрес.

**Интерфейс TAPI 2. x:** Приложения получают идентификатор адреса (и идентификатор устройства) во время вызова [**линемакекалл**](/windows/win32/api/tapi/nf-tapi-linemakecall) или [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), в структуре [**Линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo) или в вызове [**линежетаддрессид**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).

**Интерфейс TAPI 3. x:** [**Итаддресскапабилитиес:: Get \_ аддресскапабилити**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) с именем *аддресскап* , установленным в параметре [**адреса AC \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) **\_ ADDRESSID** , будет возвращать, если для параметра *плкапабилити* задано значение текущего идентификатора адреса.

 

 
