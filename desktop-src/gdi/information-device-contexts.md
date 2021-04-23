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
# <a name="information-device-contexts"></a><span data-ttu-id="4249a-103">Контексты информационных устройств</span><span class="sxs-lookup"><span data-stu-id="4249a-103">Information Device Contexts</span></span>

<span data-ttu-id="4249a-104">Information DC используется для получения данных устройства по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4249a-104">The information DC is used to retrieve default device data.</span></span> <span data-ttu-id="4249a-105">Например, приложение может вызвать функцию [**CREATE**](/windows/desktop/api/Wingdi/nf-wingdi-createica) , чтобы создать информационный контроллер домена для конкретной модели принтера, а затем вызвать функции [**жеткуррентобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) и [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) , чтобы получить атрибуты пера или кисти по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4249a-105">For example, an application can call the [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) function to create an information DC for a particular model of printer and then call the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions to retrieve the default pen or brush attributes.</span></span> <span data-ttu-id="4249a-106">Поскольку система может извлекать сведения об устройстве без создания структур, обычно связанных с другими типами устройств, информационный контроллер домена требует гораздо меньше издержек и создается значительно быстрее, чем любой другой тип.</span><span class="sxs-lookup"><span data-stu-id="4249a-106">Because the system can retrieve device information without creating the structures normally associated with the other types of device contexts, an information DC involves far less overhead and is created significantly faster than any of the other types.</span></span> <span data-ttu-id="4249a-107">После того как приложение завершит извлечение данных с помощью информационного контроллера домена, оно должно вызвать функцию [**делетедк**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="4249a-107">After an application finishes retrieving data by using an information DC, it must call the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span>

 

 



