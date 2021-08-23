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
ms.openlocfilehash: a0c66230d9e7f074fe50ca826ab196ab75a239942257899362b738296b329074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572560"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
