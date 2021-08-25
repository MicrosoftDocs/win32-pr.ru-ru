---
description: Метод Плайчаптерсаутостоп запускает воспроизведение в указанной главе по заданному названию и указанному количеству глав.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Метод Плайчаптерсаутостоп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c518496f81f4ca4e662bf8dbc821f2378cd38d27c7546356144910c0c5ba72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830744"
---
# <a name="playchaptersautostop-method"></a>Метод Плайчаптерсаутостоп

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`PlayChaptersAutoStop`Метод запускает воспроизведение в указанной главе по заданному названию и указанному количеству глав.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ититле*
</dt> <dd>

Задает заголовок в виде целочисленного значения.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ичаптер*
</dt> <dd>

Задает начальную главу как целочисленное значение.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*ичаптеркаунт*
</dt> <dd>

Указывает количество глав для воспроизведения в виде целочисленного значения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

При воспроизведении последней главы этот метод приводит к тому, что в приложение отправляется уведомление о событии [**\_ \_ \_ автозавершения в разделе с DVD-диска EC**](ec-dvd-chapter-autostop.md) .

 

 



