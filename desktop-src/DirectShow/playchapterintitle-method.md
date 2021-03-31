---
description: Метод Плайчаптеринтитле воспроизводит указанную главу в указанном заголовке.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Метод Плайчаптеринтитле
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894029"
---
# <a name="playchapterintitle-method"></a>Метод Плайчаптеринтитле

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`PlayChapterInTitle`Метод воспроизводит указанную главу в указанном заголовке.

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ититле*
</dt> <dd>

Задает заголовок в виде целочисленного значения.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ичаптер*
</dt> <dd>

Указывает главу как целочисленное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Этот метод запускает воспроизведение в указанной главе, а затем переходит в неограниченное время. Если вы хотите воспроизвести только определенную главу, используйте [**плайчаптерсаутостоп**](playchaptersautostop-method.md).

 

 



