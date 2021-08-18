---
description: Жетплайерпаренталлевел извлекает уровень родительского управления, заданный в объекте Мсвебдвд.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Метод Жетплайерпаренталлевел
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0426c48589449e03b78d894300ff2c83d83d625a269b19f0e985f78d49973f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756484"
---
# <a name="getplayerparentallevel-method"></a>Метод Жетплайерпаренталлевел

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetPlayerParentalLevel`Получает уровень родительского управления, заданный в объекте **мсвебдвд** .

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, указывающее текущий родительский уровень в навигаторе DVD, или-1, если функция родительского управления отключена.

## <a name="remarks"></a>Remarks

Приложение проигрывателя отвечает за применение родительского контроля. Родительский уровень игрока — это значение, установленное приложением, чем может быть использовано для указания самого высокого уровня родителей, который может просматривать текущий пользователь. Когда Навигатор DVD обнаруживает новый родительский уровень, используйте этот метод, чтобы определить, превышает ли новый уровень уровень, заданный приложением с помощью [**селектпаренталлевел**](selectparentallevel-method.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жеттитлепаренталлевелс**](gettitleparentallevels-method.md)
</dt> <dt>

[**жетплайерпаренталкаунтри**](getplayerparentalcountry-method.md)
</dt> <dt>

[**селектпаренталкаунтри**](selectparentalcountry-method.md)
</dt> <dt>

[**селектпаренталлевел**](selectparentallevel-method.md)
</dt> </dl>

 

 



