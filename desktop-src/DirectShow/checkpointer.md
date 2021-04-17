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
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657548"
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
| Header<br/> | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы проверки указателя](pointer-validation-macros.md)
</dt> </dl>

 

 




