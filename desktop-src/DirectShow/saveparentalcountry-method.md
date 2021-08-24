---
description: Метод Двдадм. Савепаренталкаунтри сохраняет в реестре новую страну или регион для приложения.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Метод Савепаренталкаунтри (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5391982129c799e6a565da362837a557765cf46604653f4f702ed38dcb910e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651214"
---
# <a name="saveparentalcountry-method"></a>Метод Савепаренталкаунтри

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm.SaveParentalCountry`Метод сохраняет в реестре новую страну или регион для приложения.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*икаунтри*
</dt> <dd>

Задает страну или регион в виде целого числа.

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

## <a name="remarks"></a>Remarks

Этот метод позволяет пользователю, знающему текущий пароль, сохранить в реестре новый родительский параметр страна или регион. Как и для всех методов **мсдвдадм**, этот метод не влияет на текущий уровень проигрывателя. Он изменяет только параметр реестра, чтобы при следующем создании объекта Мсвебдвд он открывался с новой страной или регионом. Чтобы изменить страну или регион в проигрывателе, вызовите [**селектпаренталкаунтри**](selectparentalcountry-method.md), который не изменяет параметр реестра.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**савепаренталлевел**](saveparentallevel-method.md)
</dt> <dt>

[Объект Мсдвдадм](msdvdadm-object.md)
</dt> </dl>

 

 




