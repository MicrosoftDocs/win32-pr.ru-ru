---
description: Метод Двдадм. Ресторескринсавер восстанавливает системные параметры экранной заставки.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Метод Ресторескринсавер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673004"
---
# <a name="restorescreensaver-method"></a>Метод Ресторескринсавер

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm.RestoreScreenSaver`Метод восстанавливает параметры экранной заставки.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Как правило, приложение DVD отключает экранную заставку системы при запуске, присвоив свойству [**дисаблескринсавер**](disablescreensaver-property.md) значение true, а затем повторно включите экранную заставку при закрытии приложения DVD с помощью вызова `RestoreScreenSaver` . Если приложение не использует параметры экранной заставки, не нужно вызывать этот метод или задавать свойство **дисаблескринсавер** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объект Мсдвдадм](msdvdadm-object.md)
</dt> </dl>

 

 



