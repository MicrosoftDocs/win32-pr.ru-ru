---
description: Обратные вызовы, используемые для просмотра текстур.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixEngine5Callbacks
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e4d672909d0d0bc332f40d672d7c658ecb5d3049
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628080"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span id="vspixengine.ipixengine5callbacks"></span>Интерфейс IPixEngine5Callbacks

Обратные вызовы, используемые для просмотра текстур.

## <a name="members"></a>Участники

Интерфейс **IPixEngine5Callbacks** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixEngine5Callbacks** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Методы

Интерфейс **IPixEngine5Callbacks** содержит следующие методы.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Метод</th><th style="text-align: left;">Описание</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>фритекстурекомплете</strong></a></td><td style="text-align: left;"><p>Функция обратного вызова, используемая для уведомления узла при освобождении текстуры.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>лоадхистограмкомплете</strong></a></td><td style="text-align: left;"><p>Функция обратного вызова, используемая для уведомления узла о завершении загрузки гистограммы.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>лоадтекстурефромфилекомплете</strong></a></td><td style="text-align: left;"><p>Функция обратного вызова, используемая для уведомления узла о завершении загрузки текстуры.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>лоадтекстуреслицекомплете</strong></a></td><td style="text-align: left;"><p>Функция обратного вызова, используемая для уведомления узла о завершении загрузки среза текстуры.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>реадтекселвалуекомплете</strong></a></td><td style="text-align: left;"><p>Функция обратного вызова, используемая для уведомления узла о завершении считывания значения шаг текселя.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>рендертекстурекомплете</strong></a></td><td style="text-align: left;"><p>Функция обратного вызова, используемая для уведомления узла о завершении прорисовки текстуры.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>саветекстурекомплете</strong></a></td><td style="text-align: left;"><p>Функция обратного вызова, используемая для уведомления узла о завершении сохранения текстуры.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 
