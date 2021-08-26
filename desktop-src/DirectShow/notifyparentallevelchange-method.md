---
description: Метод Нотифипаренталлевелчанже включает или отключает обработку событий для временных команд родительского уровня управления.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Метод Нотифипаренталлевелчанже (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8382b52f64d4196b0ef74e5f3285e9bb047a4e1f77d3b0e5bec4da218ee753b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997364"
---
# <a name="notifyparentallevelchange-method"></a>Метод Нотифипаренталлевелчанже

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`NotifyParentalLevelChange`Метод включает или отключает обработку событий для временных команд родительского уровня управления.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*бнотифи*
</dt> <dd>

Указывает логическое значение, указывающее, будет ли приложение уведомлено, когда объект Мсвебдвд встречает сегменты видео с более полной оценкой, чем общая оценка для диска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

По умолчанию уведомления родительского управления отключены. Это означает, что временные родительские команды с диска разрешены, но не учитываются, и диск будет воспроизводиться без прерывания. Вызывайте этот метод во время инициализации приложения, если необходимо управлять временными командами родительского уровня управления с диска. Чтобы отключить функцию родительского управления после ее включения, вызовите этот метод с аргументом false. Дополнительные сведения о службе родительского управления см. в разделе [**акцептпаренталлевелчанже**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**селектпаренталлевел**](selectparentallevel-method.md)
</dt> <dt>

[**жеттитлепаренталлевелс**](gettitleparentallevels-method.md)
</dt> <dt>

[**жетплайерпаренталкаунтри**](getplayerparentalcountry-method.md)
</dt> <dt>

[**жетплайерпаренталлевел**](getplayerparentallevel-method.md)
</dt> <dt>

[**селектпаренталкаунтри**](selectparentalcountry-method.md)
</dt> </dl>

 

 




