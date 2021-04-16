---
description: Функция Фонеклосе закрывает указанное телефонное устройство.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Закрытие телефонного устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543002"
---
# <a name="closing-the-phone-device"></a><span data-ttu-id="0a477-103">Закрытие телефонного устройства</span><span class="sxs-lookup"><span data-stu-id="0a477-103">Closing the Phone Device</span></span>

<span data-ttu-id="0a477-104">Функция [**фонеклосе**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) закрывает указанное телефонное устройство.</span><span class="sxs-lookup"><span data-stu-id="0a477-104">The [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) function closes the specified phone device.</span></span> <span data-ttu-id="0a477-105">Телефонное устройство можно также принудительно закрыть после того, как пользователь изменял конфигурацию этого телефона или его драйвера.</span><span class="sxs-lookup"><span data-stu-id="0a477-105">The phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="0a477-106">Если пользователь хочет, чтобы изменения конфигурации действовали немедленно (в отличие от следующей перезагрузки системы), и они влияют на текущее представление устройства (например, на возможности устройства), поставщик услуг может принудительно закрыть телефонное устройство.</span><span class="sxs-lookup"><span data-stu-id="0a477-106">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

<span data-ttu-id="0a477-107">Эти сообщения также могут быть отправлены без запроса в результате освобождения телефонного устройства каким-либо другим способом.</span><span class="sxs-lookup"><span data-stu-id="0a477-107">These messages can also be sent unsolicited as a result of the phone device being reclaimed in some other manner.</span></span> <span data-ttu-id="0a477-108">Поэтому приложение должно быть подготовлено к обработке незапрошенных [**сообщений \_ закрытия телефона**](phone-close.md) .</span><span class="sxs-lookup"><span data-stu-id="0a477-108">An application should therefore be prepared to handle unsolicited [**PHONE\_CLOSE**](phone-close.md) messages.</span></span> <span data-ttu-id="0a477-109">Во время закрытия телефонного устройства все необработанные асинхронные ответы, относящиеся к этому устройству, подавляются.</span><span class="sxs-lookup"><span data-stu-id="0a477-109">At the time the phone device is closed, any outstanding asynchronous replies pertaining to that device are suppressed.</span></span>

 

 



