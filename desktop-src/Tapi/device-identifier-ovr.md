---
description: ИДЕНТИФИКАТОР устройства — это независимый от приложения идентификатор для конкретного коммуникационного устройства.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Идентификатор устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545463"
---
# <a name="device-identifier"></a>Идентификатор устройства

*Идентификатор устройства* — это независимый от приложения идентификатор для конкретного коммуникационного устройства. Обычно это требуется, только если приложению TAPI требуется передать часть обработки, включающую в себя сеанс связи, с функциями другого API. Например, приложения TAPI 2,2 могут не иметь прямого доступа к потоку мультимедиа и могут использовать API Wave.

**Интерфейс TAPI 2. x:** См. [**линежетид**](/windows/win32/api/tapi/nf-tapi-linegetid).

**Интерфейс TAPI 3. x:** См. раздел [**итаддресскапабилитиес:: Get \_ аддресскапабилити**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*аддресскап* ) с параметром [**адреса \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) **AC \_ перманентдевицеид** .

 

 
