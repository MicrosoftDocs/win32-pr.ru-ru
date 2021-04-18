---
description: Указатель на функцию, которая вызывается из точки входа библиотеки DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Указатель функции Лпфнинитраутине (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675376"
---
# <a name="lpfninitroutine-function-pointer"></a>Указатель функции Лпфнинитраутине

Указатель на функцию, которая вызывается из точки входа библиотеки DLL.

## <a name="syntax"></a>Синтаксис


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*блоадинг* 
</dt> <dd>

**Значение true** , если библиотека DLL загружена, и **false** при выгрузке библиотеки DLL.

</dd> <dt>

*рклсид* 
</dt> <dd>

Указатель на CLISD ИНИЦИАЛИЗИРОВАННОГО объекта, указанный в переменной члена [**\_ CLSID кфакторитемплате:: m**](cfactorytemplate-m-clsid.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот указатель функции не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кфакторитемплате**](cfactorytemplate.md)
</dt> </dl>

 

 




