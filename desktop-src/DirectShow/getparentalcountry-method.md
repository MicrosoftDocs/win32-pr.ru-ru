---
description: Метод Двдадм. Жетпаренталкаунтри Извлекает родительский регион или страну, которая была сохранена в реестре в последний раз.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Метод Жетпаренталкаунтри (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeeee55a3e39449c48e1af6b2674db85d5c4a964e730e5a66bb91be6dca2c393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756764"
---
# <a name="getparentalcountry-method"></a>Метод Жетпаренталкаунтри

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm.GetParentalCountry`Метод извлекает страну или регион, которые были сохранены в реестре в последний раз.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целое число, указывающее код страны или региона по умолчанию, хранящийся в реестре.

## <a name="remarks"></a>Remarks

Родительский регион или страна, которую извлекает этот метод, не обязательно являются той же страной или регионом, которые в настоящее время хранятся в объекте Мсвебдвд.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объект Мсдвдадм](msdvdadm-object.md)
</dt> </dl>

 

 




