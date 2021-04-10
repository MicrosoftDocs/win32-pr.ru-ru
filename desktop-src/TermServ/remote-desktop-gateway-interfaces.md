---
title: Интерфейсы шлюза удаленный рабочий стол
description: Интерфейс API шлюза удаленный рабочий стол поддерживает следующие интерфейсы. Эти интерфейсы можно использовать для реализации подключаемых модулей, обеспечивающих настраиваемую проверку подлинности и авторизацию.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986205"
---
# <a name="remote-desktop-gateway-interfaces"></a>Интерфейсы шлюза удаленный рабочий стол

Интерфейс API шлюза удаленный рабочий стол поддерживает следующие интерфейсы. Эти интерфейсы можно использовать для реализации подключаемых модулей, обеспечивающих настраиваемую проверку подлинности и авторизацию. Между подключаемым модулем проверки подлинности и подключаемым модулем авторизации нет зависимостей, и при необходимости можно реализовать только один подключаемый модуль.

Подключаемые модули проверки подлинности — [**итсгаусентикатеусерсинк**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) и [**итсгаусентикатионенгине**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).

Подключаемые модули авторизации — это [**итсгаккаунтинженгине**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**итсгаусоризеконнектионсинк**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**итсгаусоризересаурцесинк**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)и [**итсгполициенгине**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**итсгаккаунтинженгине**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

Предоставляет методы, предоставляющие сведения о создании или закрытии сеансов для соединения.

</dd> <dt>

[**итсгаусентикатеусерсинк**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

Предоставляет методы, уведомляющие шлюз удаленных рабочих столов о событиях проверки подлинности.

</dd> <dt>

[**итсгаусентикатионенгине**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

Предоставляет методы, которые проверяют подлинность пользователей для шлюза удаленных рабочих столов.

</dd> <dt>

[**итсгаусоризеконнектионсинк**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

Предоставляет методы, уведомляющие шлюз удаленных рабочих столов о результатах попытки авторизации подключения.

</dd> <dt>

[**итсгаусоризересаурцесинк**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

Предоставляет методы, уведомляющие шлюз удаленных рабочих столов о результатах попытки авторизации ресурса.

</dd> <dt>

[**итсгполициенгине**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

Предоставляет методы, которые позволяют авторизовать подключения и ресурсы.

</dd> </dl>

 

 




