---
description: 'Запрос на запуск отладки шейдера. Этот запрос состоит из двух частей: создание трассировки и отладка трассировки.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IDebugShaderRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11df1b8bb4eead01ae374a1af4e058464ccb55fb
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786180"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span id="vspixengine.idebugshaderrequest2"></span>Интерфейс IDebugShaderRequest2

Запрос на запуск отладки шейдера. Этот запрос состоит из двух частей: создание трассировки и отладка трассировки.

## <a name="members"></a>Элементы

Интерфейс **IDebugShaderRequest2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDebugShaderRequest2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Методы

Интерфейс **IDebugShaderRequest2** содержит следующие методы.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Метод</th><th >Описание</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>бегиндебугшадер</strong></a></td><td ><p>Запросы на запуск отладки указанного списка инструкций.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>женератеинструктионс</strong></a></td><td ><p>Запросы на создание инструкций трассировки шейдера в отладочном запросе. Отладка на основе трассировки происходит в ЦП (деформацию), а не на GPU.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 
