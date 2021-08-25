---
description: Information DC используется для получения данных устройства по умолчанию.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Контексты информационных устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974b861f47ffbd19566a5224d0c2705e9797e86abbe46005c6eb1687a9573378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779134"
---
# <a name="information-device-contexts"></a>Контексты информационных устройств

Information DC используется для получения данных устройства по умолчанию. Например, приложение может вызвать функцию [**CREATE**](/windows/desktop/api/Wingdi/nf-wingdi-createica) , чтобы создать информационный контроллер домена для конкретной модели принтера, а затем вызвать функции [**жеткуррентобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) и [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) , чтобы получить атрибуты пера или кисти по умолчанию. Поскольку система может извлекать сведения об устройстве без создания структур, обычно связанных с другими типами устройств, информационный контроллер домена требует гораздо меньше издержек и создается значительно быстрее, чем любой другой тип. После того как приложение завершит извлечение данных с помощью информационного контроллера домена, оно должно вызвать функцию [**делетедк**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .

 

 



