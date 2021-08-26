---
description: Проверяет, имеет ли указатель значение NULL. Если указатель имеет значение NULL, функция или метод, в которых отображается макрос, возвращает указанное значение.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Макрос контрольной точки (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ef1fa2370def45321958862ebaf3ded341b13f45ddae1ecafdc4a17e937aca08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999294"
---
# <a name="checkpointer-macro"></a>Макрос контрольной точки

Проверяет, имеет ли указатель **значение NULL**. Если указатель имеет **значение NULL**, функция или метод, в которых отображается макрос, возвращает указанное значение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ш* 
</dt> <dd>

Указатель на проверку.

</dd> <dt>

*обратно* 
</dt> <dd>

Значение, возвращаемое функцией или методом, если *p* имеет **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Окружающая функция возвращает *RET* , если *p* имеет **значение NULL**. В противном случае макрос не будет возвращать окружающую функцию.

## <a name="examples"></a>Примеры


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы проверки указателя](pointer-validation-macros.md)
</dt> </dl>

 

 




