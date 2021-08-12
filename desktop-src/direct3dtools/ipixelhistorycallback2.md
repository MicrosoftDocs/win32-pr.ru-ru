---
description: Обратный вызов для возврата пересечения журнала пикселей (прорисовки уровня вызова) и примитивов (уровень треугольника) в двух разных результатах.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixelHistoryCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ccb3ea0f3e3cdffbe0b3469b1897d4081eaff89a9ffa4e7eaf43217664f57d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283229"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span id="vspixengine.ipixelhistorycallback2"></span>Интерфейс IPixelHistoryCallback2

Обратный вызов для возврата пересечения журнала пикселей (прорисовки уровня вызова) и примитивов (уровень треугольника) в двух разных результатах.

## <a name="members"></a>Элементы

Интерфейс **IPixelHistoryCallback2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixelHistoryCallback2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Методы

Интерфейс **IPixelHistoryCallback2** содержит следующие методы.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Метод</th><th style="text-align: left;">Описание</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>интерсектионскаллбакк</strong></a></td><td style="text-align: left;"><p>Обратный вызов, уведомляющий узел о размещении сведений о пересечении журнала пикселей, возвращаемых запросом связана.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>примитивескаллбакк</strong></a></td><td style="text-align: left;"><p>Обратный вызов, уведомляющий узел о том, что сведения о операции примитива журнала пикселей возвращены связанным запросом.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 
