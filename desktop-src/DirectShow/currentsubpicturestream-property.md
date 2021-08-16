---
description: Свойство Куррентсубпиктурестреам задает или получает текущий поток субтитров.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Куррентсубпиктурестреам, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c4af677180d4893ef56a9d2bff1fb034971969e2e64d648d53e19d0814a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821949"
---
# <a name="currentsubpicturestream-property"></a>Куррентсубпиктурестреам, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentSubpictureStream`Свойство задает или получает текущий поток субтитров.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее поток.

## <a name="remarks"></a>Remarks

Возможные значения этого свойства:



| Значение   | Описание              |
|---------|--------------------------|
| от 0 до 31 | Поток субтитров    |
| 63      | Выключение потока с низкой скоростью |



 

Это свойство доступно для чтения и записи и не имеет значения по умолчанию. Перед настройкой нового потока субтитров вызовите [**иссубпиктурестреаменаблед**](issubpicturestreamenabled-method.md) , чтобы убедиться, что поток доступен.

Установка этого свойства приводит к тому, что свойство [**субпиктуреон**](subpictureon-property.md) переключается в **true**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**субпиктуреон**](subpictureon-property.md)
</dt> <dt>

[**субпиктурестреамсаваилабле**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



