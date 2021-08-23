---
description: Число потоков потоковой передачи, использующих этот ПИН-код.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Элемент Кдинамикаутпутпин:: m_dwNumOutstandingOutputPinUsers (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29fc593065af4252f58ce4bb08dd41fac82926dc11490377f6a8af614794b22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688714"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>Элемент Кдинамикаутпутпин:: m \_ двнумаутстандингаутпутпинусерс

Число потоков потоковой передачи, использующих этот ПИН-код.

## <a name="syntax"></a>Синтаксис


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Remarks

Метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) увеличивает эту переменную, а метод [**Кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) уменьшает его. Если значение больше нуля, то некоторый поток использует этот ПИН-код для потоковой передачи данных или для изменения типа соединения. ПИН-код не может быть заблокирован, пока это так.

Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> <dt>

[**Кдинамикаутпутпин:: Стреамингсреадусингаутпутпин**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




