---
description: Свойство Субпиктурестреамсаваилабле извлекает количество потоков субтитров, доступных в текущем заголовке.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Субпиктурестреамсаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684394"
---
# <a name="subpicturestreamsavailable-property"></a>Субпиктурестреамсаваилабле, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SubpictureStreamsAvailable`Свойство получает количество потоков субтитров, доступных в текущем заголовке.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество доступных потоков в виде целого числа.

## <a name="remarks"></a>Комментарии

Это свойство доступно только для чтения и не имеет значения по умолчанию. Чтобы запросить каждый поток для своего атрибута языка, сначала вызовите этот метод, чтобы получить верхнюю границу.

Нумерация потоков отсчитывается от нуля.

 

 



