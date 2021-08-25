---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d144374f690d295b80d0092add56439eb4e5fc9d546ba1f970ab99976cf2d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888398"
---
# <a name="iagentballoongetenabled"></a>Иажентбаллун:: enable

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




