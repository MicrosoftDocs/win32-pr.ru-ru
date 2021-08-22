---
description: Метод Двдадм. Ресторескринсавер восстанавливает системные параметры экранной заставки.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Метод Ресторескринсавер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 684250b237105e391472237a5e7093855dd82ef5b59ffbbaa20ebecf386da302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696974"
---
# <a name="restorescreensaver-method"></a>Метод Ресторескринсавер

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm.RestoreScreenSaver`Метод восстанавливает параметры экранной заставки.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Как правило, приложение DVD отключает экранную заставку системы при запуске, присвоив свойству [**дисаблескринсавер**](disablescreensaver-property.md) значение true, а затем повторно включите экранную заставку при закрытии приложения DVD с помощью вызова `RestoreScreenSaver` . Если приложение не использует параметры экранной заставки, не нужно вызывать этот метод или задавать свойство **дисаблескринсавер** .

## <a name="see-also"></a>См. также

<dl> <dt>

[Объект Мсдвдадм](msdvdadm-object.md)
</dt> </dl>

 

 



