---
description: Свойство Субпиктуреон задает или получает текущее состояние подизображения (on или OFF).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Субпиктуреон, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692df6b69bc960562e9acd223a0e4e156fe00de2206146f609ba15d550b7a961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951773"
---
# <a name="subpictureon-property"></a>Субпиктуреон, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SubpictureOn`Свойство задает или получает текущее состояние подизображения (on или OFF).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение, указывающее, отображается ли подизображение.

## <a name="remarks"></a>Remarks

Это свойство не влияет на отображение скрытых субтитров. Скрытые субтитры внедряются в поток видео. Подизображения DVD передаются в отдельном потоке.

Когда поток субтитров изменяется с помощью [**куррентсубпиктурестреам**](currentsubpicturestream-property.md), `SubpictureOn` свойство переключается на **true**.

Это свойство доступно для чтения и записи со значением по умолчанию false.

 

 



