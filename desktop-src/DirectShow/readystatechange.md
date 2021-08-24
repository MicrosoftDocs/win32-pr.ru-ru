---
description: Событие Реадистатечанже отправляется при изменении свойства ReadyState элемента управления Мсвебдвд.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: реадистатечанже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f73e0b5b7cd7178df31b3f6efda56e398d8cb406598355a3c49702714686af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697124"
---
# <a name="readystatechange"></a>реадистатечанже

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ReadyStateChange`Событие отправляется при изменении свойства **ReadyState** элемента управления мсвебдвд.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*
</dt> <dd>

Указывает новое значение свойства [**ReadyState**](readystate-property.md) .



| Значение | Описание               |
|-------|---------------------------|
| 0     | НАЗВАНИЕ READYSTATE не \_ инициализировано |
| 1     | \_Загрузка READYSTATE       |
| 2     | READYSTATE \_ загружен        |
| 3     | READYSTATE \_ Interactive   |
| 4     | READYSTATE \_ завершен      |



 

</dd> </dl>

 

 



