---
description: Прежде чем сокет можно будет использовать для настройки соединения или получения запроса на подключение, он должен быть привязан к локальному адресу.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Привязка к локальному адресу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd4691e6581cbe1a3a2dee21d7dc4e0a0672812121028c515ad192b30279f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132757"
---
# <a name="binding-to-a-local-address"></a>Привязка к локальному адресу

Прежде чем сокет можно будет использовать для настройки соединения или получения запроса на подключение, он должен быть привязан к локальному адресу. Это можно сделать явным образом, вызвав [**вспбинд**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))или неявно [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , если сокет не привязан при вызове этой функции.

 

 
