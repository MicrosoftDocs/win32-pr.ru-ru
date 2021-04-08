---
title: Иажентаудиуутпутпропертиес
description: Иажентаудиуутпутпропертиес
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067932"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a>Иажентаудиуутпутпропертиес:: enable

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

Получает значение, указывающее, включен ли речевой вывод символов.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если речевой вывод включен и **значение false** в случае отключения.

</dd> </dl>

Поскольку этот параметр влияет на речевой вывод (TTS и звуковой файл) для всех символов, только пользователь может изменить это свойство на странице свойств Microsoft Agent.

 

 




