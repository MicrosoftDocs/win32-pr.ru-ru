---
title: Иажентаудиуутпутпропертиес Жетусингсаундеффектс
description: Иажентаудиуутпутпропертиес Жетусингсаундеффектс
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776175"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>Иажентаудиуутпутпропертиес:: Жетусингсаундеффектс

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

Получает значение, указывающее, включен ли вывод звуковых эффектов.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*пбусингсаундеффектс*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если в настоящий момент включен вывод звуковых эффектов и **значение false** в случае отключения.

</dd> </dl>

Звуковые эффекты для анимации символа назначаются в редакторе символов Microsoft Agent. Поскольку этот параметр влияет на вывод звуковых эффектов для всех символов, только пользователь может изменить это свойство на странице свойств Microsoft Agent.

 

 




