---
description: Метод DVDTimeCode2bstr извлекает строку, указывающую текущее время на диске.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Метод DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bda68bafa462af5d425c62368b51f8b4b08ce2dfc310276e8f26b7c4601fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148607"
---
# <a name="dvdtimecode2bstr-method"></a>Метод DVDTimeCode2bstr

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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

## <a name="remarks"></a>Remarks

Этот метод доступен только для чтения.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обработка уведомлений о событиях DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



