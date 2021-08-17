---
title: Иаженткоммандвиндов Сетвисибле
description: Иаженткоммандвиндов Сетвисибле
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8d06c40fd88b525cadf9f90a1edd4edaaf3a9e9be7ccdcfa98dd6abf8b833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692647"
---
# <a name="iagentcommandwindowsetvisible"></a>Иаженткоммандвиндов:: Сетвисибле

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Установите свойство [**Visible**](visible-property.md) для окна "Voice Commands".

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*
</dt> <dd>

Параметр [**видимого**](visible-property.md) свойства. Значение **true** отображает окно "Voice Commands"; **Значение false** скрывает его.

</dd> </dl>

Пользователь может переопределить это свойство.

## <a name="see-also"></a>См. также

[**Иаженткоммандвиндов:: Visible**](iagentcommandwindow--getvisible.md)


 

 




