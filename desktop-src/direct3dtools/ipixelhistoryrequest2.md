---
description: Запрашивать пересечения и примитивы журнала пикселей отдельно.
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixelHistoryRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e4fc6c450a2ac31dc364ed20f4eb466ca0ae4d99
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622550"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span id="vspixengine.ipixelhistoryrequest2"></span>Интерфейс IPixelHistoryRequest2

Запрашивать пересечения и примитивы журнала пикселей отдельно.

## <a name="members"></a>Участники

Интерфейс **IPixelHistoryRequest2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixelHistoryRequest2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Методы

Интерфейс **IPixelHistoryRequest2** содержит следующие методы.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Метод</th><th style="text-align: left;">Описание</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>рекуестинтерсектионс</strong></a></td><td style="text-align: left;"><p>Запрашивает список событий, которые вызывают изменение в указанном пикселе, прорисовку целевого объекта/UAV и кадра.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>рекуестпримитивес</strong></a></td><td style="text-align: left;"><p>Запрашивает список примитивов из определенного пересечения. Дополнительные сведения см. в описании функции члена Рекуестинтерсектионс.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 
