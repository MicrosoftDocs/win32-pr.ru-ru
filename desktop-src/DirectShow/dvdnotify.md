---
description: Событие Двднотифи уведомляет приложение о различных событиях и дисках DVD.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: Двднотифи (сегмент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675756"
---
# <a name="dvdnotify"></a>двднотифи

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

Это `DVDNotify` событие уведомляет приложение о различных событиях и дисках DVD.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Указывает код уведомления о событии DVD.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Параметр1*
</dt> <dd>

Может содержать дополнительные сведения, относящиеся к событию.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Может содержать дополнительные сведения, относящиеся к событию.

</dd> </dl>

## <a name="remarks"></a>Комментарии

[Коды уведомлений о событиях DVD](dvd-notification-codes.md) предоставляют полное описание всех кодов уведомлений о событиях DVD и их параметров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



 

 




