---
description: Метод Плайчаптеринтитле воспроизводит указанную главу в указанном заголовке.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Метод Плайчаптеринтитле
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407684ecf8db6053a4d166a4ed069f9cabf0b36f983dd04bfdf9cf85e6c8dc2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830874"
---
# <a name="playchapterintitle-method"></a>Метод Плайчаптеринтитле

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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

## <a name="remarks"></a>Remarks

Этот метод запускает воспроизведение в указанной главе, а затем переходит в неограниченное время. Если вы хотите воспроизвести только определенную главу, используйте [**плайчаптерсаутостоп**](playchaptersautostop-method.md).

 

 



