---
description: Information DC используется для получения данных устройства по умолчанию.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Контексты информационных устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544458"
---
# <a name="information-device-contexts"></a>Контексты информационных устройств

Information DC используется для получения данных устройства по умолчанию. Например, приложение может вызвать функцию [**CREATE**](/windows/desktop/api/Wingdi/nf-wingdi-createica) , чтобы создать информационный контроллер домена для конкретной модели принтера, а затем вызвать функции [**жеткуррентобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) и [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) , чтобы получить атрибуты пера или кисти по умолчанию. Поскольку система может извлекать сведения об устройстве без создания структур, обычно связанных с другими типами устройств, информационный контроллер домена требует гораздо меньше издержек и создается значительно быстрее, чем любой другой тип. После того как приложение завершит извлечение данных с помощью информационного контроллера домена, оно должно вызвать функцию [**делетедк**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .

 

 



