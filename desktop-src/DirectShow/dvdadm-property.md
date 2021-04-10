---
description: Свойство Двдадм предоставляет доступ к объекту Мсдвдадм, содержащему методы и свойства для сохранения сведений о приложении и пользователе.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Двдадм, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140042"
---
# <a name="dvdadm-property"></a>Двдадм, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm`Свойство предоставляет доступ к объекту [мсдвдадм](msdvdadm-object.md) , содержащему методы и свойства для сохранения сведений о приложении и пользователе.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Комментарии

Это свойство доступно только для чтения и не имеет значения по умолчанию. Нет необходимости создавать отдельную ссылку на объект **мсдвдадм** . Чтобы получить доступ к методам и свойствам объекта, используйте `DVDAdm` свойство, как показано в следующем примере.

## <a name="examples"></a>Примеры


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



