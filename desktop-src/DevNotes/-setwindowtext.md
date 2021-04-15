---
description: Изменяет текст заголовка указанного окна (если он имеется).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: Функция _SetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649041"
---
# <a name="_setwindowtext-function"></a>\_Функция SetWindowText

\[Эта функция является оболочкой для функции **SetWindowText** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать **SetWindowText** напрямую.\]

Изменяет текст заголовка указанного окна (если он имеется). См. [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).

## <a name="syntax"></a>Синтаксис


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
