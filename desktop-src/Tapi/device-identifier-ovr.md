---
description: ИДЕНТИФИКАТОР устройства — это независимый от приложения идентификатор для конкретного коммуникационного устройства.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Идентификатор устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19078b7d2774fb2b71d951fade9c7a560a597a188ac4d87982ee2a6f2bfc9416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946002"
---
# <a name="device-identifier"></a>Идентификатор устройства

*Идентификатор устройства* — это независимый от приложения идентификатор для конкретного коммуникационного устройства. Обычно это требуется, только если приложению TAPI требуется передать часть обработки, включающую в себя сеанс связи, с функциями другого API. Например, приложения TAPI 2,2 могут не иметь прямого доступа к потоку мультимедиа и могут использовать API Wave.

**Интерфейс TAPI 2. x:** См. [**линежетид**](/windows/win32/api/tapi/nf-tapi-linegetid).

**Интерфейс TAPI 3. x:** См. раздел [**итаддресскапабилитиес:: Get \_ аддресскапабилити**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*аддресскап* ) с параметром [**адреса \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) **AC \_ перманентдевицеид** .

 

 
