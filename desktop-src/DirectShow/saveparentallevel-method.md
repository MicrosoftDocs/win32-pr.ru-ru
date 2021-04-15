---
description: Метод Двдадм. Савепаренталлевел сохраняет новый родительский уровень по умолчанию в реестре.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Метод Савепаренталлевел (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675613"
---
# <a name="saveparentallevel-method"></a>Метод Савепаренталлевел

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

Метод **двдадм. савепаренталлевел** сохраняет новый родительский уровень по умолчанию в реестре.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*илевел*
</dt> <dd>

Задает родительский уровень в качестве значения anInteger от 1 до 8.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*
</dt> <dd>

Указывает имя пользователя в виде строки. (В настоящий момент игнорируется.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*
</dt> <dd>

Указывает пароль в виде строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Этот метод позволяет пользователю, знающему текущий пароль, сохранить новый параметр родительского уровня в реестре. Как и для всех методов **мсдвдадм**, этот метод не влияет на текущий уровень проигрывателя. Он изменяет только параметр реестра, чтобы при следующем запуске объекта Мсвебдвд он открывался с новым уровнем. Укажите значение-1, чтобы отключить функцию родительского управления. Чтобы изменить родительский уровень в проигрывателе, вызовите [**селектпаренталлевел**](selectparentallevel-method.md), который не изменяет параметр реестра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объект Мсдвдадм](msdvdadm-object.md)
</dt> </dl>

 

 




