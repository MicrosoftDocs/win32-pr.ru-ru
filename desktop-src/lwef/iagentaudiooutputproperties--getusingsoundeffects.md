---
title: Иажентаудиуутпутпропертиес Жетусингсаундеффектс
description: Иажентаудиуутпутпропертиес Жетусингсаундеффектс
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750dbfee36039337025a03b9f77573a2134f85d15a56d77b2d512482c7bb0e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751458"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>Иажентаудиуутпутпропертиес:: Жетусингсаундеффектс

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




