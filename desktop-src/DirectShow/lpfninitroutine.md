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
ms.openlocfilehash: c07f22b9dc261fe9d7b073a1f1ab93aa49e482fb70c53288aeaf606e6be9aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685084"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кфакторитемплате**](cfactorytemplate.md)
</dt> </dl>

 

 




