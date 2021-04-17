---
description: Свойство Субпиктуреон задает или получает текущее состояние подизображения (on или OFF).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Субпиктуреон, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684395"
---
# <a name="subpictureon-property"></a>Субпиктуреон, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SubpictureOn`Свойство задает или получает текущее состояние подизображения (on или OFF).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение, указывающее, отображается ли подизображение.

## <a name="remarks"></a>Комментарии

Это свойство не влияет на отображение скрытых субтитров. Скрытые субтитры внедряются в поток видео. Подизображения DVD передаются в отдельном потоке.

Когда поток субтитров изменяется с помощью [**куррентсубпиктурестреам**](currentsubpicturestream-property.md), `SubpictureOn` свойство переключается на **true**.

Это свойство доступно для чтения и записи со значением по умолчанию false.

 

 



