---
title: Недопустимый тип ресурса D1106
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: Данный ресурс имеет тип, отличный от ожидаемого.
keywords:
- Недопустимый тип ресурса D1106 Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105649145"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106: недопустимый тип ресурса

Указанный ресурс ресурса \[  \] не имеет ожидаемого типа.

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*ресурсов*
</dt> <dd>

Адрес ресурса.

</dd> </dl> 




 

## <a name="possible-causes"></a>Возможные причины

Интерфейс был неправильно приведен и использован в качестве параметра для метода или функции.

## <a name="examples"></a>Примеры

В следующем примере объект [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) передается, когда ожидается [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



В этом примере создается следующее сообщение отладки:

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a>Исправления

Используйте тип, требуемый для метода.

 

 
