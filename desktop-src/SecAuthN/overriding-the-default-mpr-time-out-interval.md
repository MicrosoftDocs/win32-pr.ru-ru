---
description: Маршрутизатор с несколькими поставщиками (MPR) вызывает Нпжеткапс, чтобы узнать, когда будут запущены поставщики сети (Ниндекс имеет значение ВННК \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Переопределение интервала времени ожидания MPR по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999094"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Переопределение интервала времени ожидания MPR по умолчанию

[*Маршрутизатор с несколькими поставщиками*](../secgloss/m-gly.md) (MPR) вызывает [**нпжеткапс**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) , чтобы узнать, когда будут запущены поставщики сети (*ниндекс* имеет значение вннк \_ Start). Затем многопротокольный маршрутизатор ожидает превышение времени ожидания, заданное всеми поставщиками сети, прежде чем он предоставит объединенную сеть пользователю. Если один из сетевых поставщиков не знает, когда он начнется, то для этого поставщика используется время ожидания по умолчанию (60 секунд).

При необходимости администратор может переопределить время ожидания по умолчанию, создав следующий реестр реестра с регистром **\_ DWORD** , где *n* — интервал времени ожидания в миллисекундах:

**HKey \_ \_** \\  \\  \\ **Элемент управления** CurrentControlSet системы локального компьютера \\ **нетворкпровидер** \\ **ресторетимеаут**  =  *n*

В следующем псевдокоде показан полный логический поток для обработки истечения времени ожидания многопротокольного алгоритма.


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
