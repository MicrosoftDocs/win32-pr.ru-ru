---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332467"
---
# <a name="iagentballoongetenabled"></a>Иажентбаллун:: enable

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Извлекает значение свойства [**Enabled**](enabled-property.md) для всплывающей подсказки.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*
</dt> <dd>

Адрес переменной, которая получает **значение true** , если всплывающее сообщение Word включено, и **значение false** , если оно отключено.

</dd> </dl>

Сервер Microsoft Agent автоматически отображает всплывающую подсказку для речевого вывода, если она не отключена. Всплывающая подсказка может быть отключена для символа в редакторе символов Microsoft Agent или (пользователем) для всех символов на странице свойств Microsoft Agent. Если пользователь отключает всплывающую подсказку, клиент не может восстановить его.

 

 




