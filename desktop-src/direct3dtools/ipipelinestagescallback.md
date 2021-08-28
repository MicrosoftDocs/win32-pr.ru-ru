---
description: <span id="vspixengine.ipipelinestagescallback"></span>Интерфейс Ипипелинестажескаллбакк — не используется. Ранее он является обратным вызовом для данных стадий конвейера.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ипипелинестажескаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2fc828d902f1daa3b2c0c75d2f22671d9bdec942
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787507"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span id="vspixengine.ipipelinestagescallback"></span>Интерфейс Ипипелинестажескаллбакк

Не используется. Ранее он является обратным вызовом для данных стадий конвейера.

## <a name="members"></a>Элементы

Интерфейс **ипипелинестажескаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ипипелинестажескаллбакк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Методы

Интерфейс **ипипелинестажескаллбакк** содержит следующие методы.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Метод</th><th >Описание</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>жетсуппортедстажес</strong></a></td><td ><p>Обратный вызов, уведомляющий узел о том, какие этапы конвейера используются вызовом Draw запроса связана.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>мешдатанотаваилаблекаллбакк</strong></a></td><td ><p>Обратный вызов, уведомляющий узел о том, какие этапы конвейера не могут вернуть данные сетки для события, указанного в связанном запросе.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>мешдатаверткаллбакк</strong></a></td><td ><p>Обратный вызов, уведомляющий узел о том, что данные сетки этапа конвейера возвращены запросом связана.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ресулткаллбакк</strong></a></td><td ><p>Обратный вызов, уведомляющий узел о том, что данные образа этапа конвейера возвращены запросом связана.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 
