---
description: Обратный вызов из обработчика, указывающий, что он завершил анализ всех новых кадров, добавленных в журнал.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Иневфрамескаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f9d47e84cf4deeebafa6592853f73e86d8339f8
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787320"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>Интерфейс Иневфрамескаллбакк

Обратный вызов из обработчика, указывающий, что он завершил анализ всех новых кадров, добавленных в журнал.

## <a name="members"></a>Элементы

Интерфейс **иневфрамескаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иневфрамескаллбакк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Методы

Интерфейс **иневфрамескаллбакк** содержит следующие методы.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Метод</th><th >Описание</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>канцелалл</strong></a></td><td ><p>Обратный вызов, уведомляющий узел о том, что все запросы отменены.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>канцелусингкаллбакк</strong></a></td><td ><p>Обратный вызов, уведомляющий узел об отмене запроса.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>канцелусингкукие</strong></a></td><td ><p>Обратный вызов, уведомляющий узел об отмене запроса с помощью файла cookie, уникально идентифицирующего запрос.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>невфрамесаваилабле</strong></a></td><td ><p>Обратный вызов, уведомляющий основное приложение о том, что новые кадры доступны для обработки.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 
