---
description: Метод Двдадм. Жетпаренталкаунтри Извлекает родительский регион или страну, которая была сохранена в реестре в последний раз.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Метод Жетпаренталкаунтри (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652109"
---
# <a name="getparentalcountry-method"></a>Метод Жетпаренталкаунтри

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`DVDAdm.GetParentalCountry`Метод извлекает страну или регион, которые были сохранены в реестре в последний раз.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целое число, указывающее код страны или региона по умолчанию, хранящийся в реестре.

## <a name="remarks"></a>Комментарии

Родительский регион или страна, которую извлекает этот метод, не обязательно являются той же страной или регионом, которые в настоящее время хранятся в объекте Мсвебдвд.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Сегмент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объект Мсдвдадм](msdvdadm-object.md)
</dt> </dl>

 

 




