---
description: Указатель на функцию, которая вызывается из точки входа библиотеки DLL. Может иметь значение NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Элемент Кфакторитемплате:: m_lpfnInit (Комбасе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657570"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>Элемент Кфакторитемплате:: m \_ лпфнинит

Указатель на функцию, которая вызывается из точки входа библиотеки DLL. Может иметь **значение NULL**.

## <a name="syntax"></a>Синтаксис


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Примечания

Тип указателя функции — [**лпфнинитраутине**](lpfninitroutine.md). При предоставлении этой функции в библиотеке DLL функция точки входа DLL вызывает ее со следующими параметрами:

-   *блоадинг*: **true** при загрузке библиотеки DLL, **значение false** при выгрузке библиотеки DLL.
-   *рклсид*: указатель на clisd инициализированного объекта, указанный в переменной члена [**\_ CLSID кфакторитемплате:: m**](cfactorytemplate-m-clsid.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кфакторитемплате**](cfactorytemplate.md)
</dt> </dl>

 

 




