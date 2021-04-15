---
title: D1114 не Необязательный указатель NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'Параметр интерфейса:: method является необязательным. Передан пустой указатель. Это приведет к сбою Direct2D.'
keywords:
- D1114 Необязательный указатель NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105649143"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114: Необязательный указатель NULL

Параметр параметра \[  \] *интерфейса*::*method* является необязательным. Передан **пустой** указатель. Это приведет к сбою Direct2D.

### <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*параметр*
</dt> <dd>

Имя параметра, содержащего указатель **null** .

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*
</dt> <dd>

Имя интерфейса, которому принадлежит *метод* .

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Method*
</dt> <dd>

Имя метода, получившего недопустимый параметр.

</dd> </dl> 




 

### <a name="examples"></a>Примеры

В следующем примере показано, что метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) получает указатель null для необязательного параметра *Geometry* .


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



В этом примере создается следующее сообщение отладки:

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Возможные причины

Для необязательного параметра был передан пустой указатель.

## <a name="fixes"></a>Исправления

Убедитесь, что необязательный параметр не имеет ПУСТого указателя.

 

 
