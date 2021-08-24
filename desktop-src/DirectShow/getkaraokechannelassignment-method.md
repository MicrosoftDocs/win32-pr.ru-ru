---
description: Метод Жеткараокечаннелассигнмент извлекает значение, которое указывает, как каналы караоке назначаются для динамиков.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Метод Жеткараокечаннелассигнмент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010e8112ece9b3fc66831055995ebf46657d4216942ac3b9dee05b1b68d18761
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812554"
---
# <a name="getkaraokechannelassignment-method"></a>Метод Жеткараокечаннелассигнмент

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetKaraokeChannelAssignment`Метод получает значение, указывающее, как каналы караоке назначаются динамикам.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Задает аудиопоток в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целое число, указывающее назначение динамика для указанного потока.



| Код возврата | Описание                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | Поток назначается левому и правому колонкам.                  |
| 3           | Поток назначается левым, правым и средним динамиками.         |
| 4           | Поток назначается левым, правым и audio1 докладчиками.         |
| 5           | Поток назначается левым, правым, средним и audio1 докладчиками. |
| 6           | Поток назначается левым, правым и Audio2 докладчиками.         |
| 7           | Поток назначается левым, правым, средним и Audio2 докладчиками. |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**караокеаудиопресентатионмоде**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



