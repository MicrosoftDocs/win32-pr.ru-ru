---
description: Свойство Двдадм предоставляет доступ к объекту Мсдвдадм, содержащему методы и свойства для сохранения сведений о приложении и пользователе.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Двдадм, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adedea036393e68456cfd9f035882ae9c335063030518e808c57bced6d5b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079164"
---
# <a name="dvdadm-property"></a>Двдадм, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm`Свойство предоставляет доступ к объекту [мсдвдадм](msdvdadm-object.md) , содержащему методы и свойства для сохранения сведений о приложении и пользователе.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Remarks

Это свойство доступно только для чтения и не имеет значения по умолчанию. Нет необходимости создавать отдельную ссылку на объект **мсдвдадм** . Чтобы получить доступ к методам и свойствам объекта, используйте `DVDAdm` свойство, как показано в следующем примере.

## <a name="examples"></a>Примеры


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



