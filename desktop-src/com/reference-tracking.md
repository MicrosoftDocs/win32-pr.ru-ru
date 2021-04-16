---
title: Отслеживание ссылок
description: Отслеживание ссылок
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488317"
---
# <a name="reference-tracking"></a>Отслеживание ссылок

Отслеживание ссылок может препятствовать непреднамеренной или вредоносной ранней версии объектов.

При включении отслеживания ссылок вы запрашиваете, что распределенные вызовы [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) и [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) проходят проверку подлинности с помощью COM. Когда отслеживание ссылок включено, COM отслеживает счетчики ссылок на пользователей, чтобы пользователь мог вызывать **выпуск** только для тех объектов, для которых пользователь ранее назывался **AddRef** . Несмотря на то, что отслеживание ссылок может снизить производительность, это гарантирует, что независимо от того, сколько раз заданный пользователь вызывает **выпуск**, объекты и заглушки будут существовать, если у кого-то другого есть ссылка на них.

Клиент может настроить отслеживание ссылок для процесса, передав \_ флаг еоак Secure \_ REFS в вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Можно также включить или отключить отслеживание ссылок для всех приложений на компьютере с помощью Dcomcnfg.exe.

Если включено отслеживание ссылок, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) всегда использует параметры безопасности по умолчанию. В этом случае вызовы метода [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) на **IUnknown** завершатся ошибкой.

 

 