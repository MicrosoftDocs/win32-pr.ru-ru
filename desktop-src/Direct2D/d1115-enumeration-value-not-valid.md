---
title: Недопустимое значение перечисления D1115
description: Недопустимое значение перечисления D1115
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Недопустимое значение перечисления D1115 Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105649169"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115: недопустимое значение перечисления

Параметр параметра \[  \] со \[ *значением* \] *интерфейса*::*method* не является допустимым значением перечисления.

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*параметр*
</dt> <dd>

Имя параметра, получившего непредвиденный тип.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*значений*
</dt> <dd>

Недопустимое значение перечисления.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*
</dt> <dd>

Имя интерфейса, которому принадлежит *метод* .

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Method*
</dt> <dd>

Имя метода, получившего недопустимое значение перечисления.

</dd> </dl> 




 

## <a name="examples"></a>Примеры

В следующем примере задается значение перечисления [**\_ \_ \_ типа целевого объекта отрисовки D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) , равное 30, которое находится за пределами ожидаемого диапазона.


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



В этом примере создается следующее сообщение отладки:

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>Возможные причины

Параметр использовал недопустимое значение перечисления.

## <a name="fixes"></a>Исправления

Используйте допустимое значение перечисления.

> [!Note]  
> В настоящее время слой отладки проверяет только отдельные значения перечисления. Он не проверяет, является ли побитовое сочетание допустимым.

 

 

 
