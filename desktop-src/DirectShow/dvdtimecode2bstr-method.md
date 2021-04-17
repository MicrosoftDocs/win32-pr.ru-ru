---
description: Метод DVDTimeCode2bstr извлекает строку, указывающую текущее время на диске.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Метод DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673033"
---
# <a name="dvdtimecode2bstr-method"></a>Метод DVDTimeCode2bstr

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDTimeCode2bstr`Метод получает строку, указывающую текущее время на диске.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*стимекоде*
</dt> <dd>

Указывает текущее время на диске относительно начала заголовка в виде числа, полученного с помощью события [**\_ \_ хмсф Current в текущем \_ \_ времени**](ec-dvd-current-hmsf-time.md) в формате "DVD".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает строку из 11 символов в формате "чч: мм: СС: FF", представляющей часы, минуты, секунды и кадры, определяющие текущее время.

## <a name="remarks"></a>Комментарии

Этот метод доступен только для чтения.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обработка уведомлений о событиях DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



