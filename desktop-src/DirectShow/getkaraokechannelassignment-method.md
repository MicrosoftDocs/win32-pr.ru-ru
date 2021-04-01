---
description: Метод Жеткараокечаннелассигнмент извлекает значение, которое указывает, как каналы караоке назначаются для динамиков.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Метод Жеткараокечаннелассигнмент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895229"
---
# <a name="getkaraokechannelassignment-method"></a>Метод Жеткараокечаннелассигнмент

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**караокеаудиопресентатионмоде**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



