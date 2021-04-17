---
description: Расширения интерфейса IPixEngine4, содержащие дополнения для просмотра текстур.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537190"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span id="vspixengine.ipixengine5"></span>Интерфейс IPixEngine5

Расширения интерфейса IPixEngine4, содержащие дополнения для просмотра текстур.

## <a name="members"></a>Элементы

Интерфейс **IPixEngine5** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixEngine5** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Методы

Интерфейс **IPixEngine5** содержит следующие методы.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Метод</th><th style="text-align: left;">Описание</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>фритекстуреасинк</strong></a></td><td style="text-align: left;"><p>Освобождает текстуру и уведомляет узел асинхронно.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>лоадхистограмасинк</strong></a></td><td style="text-align: left;"><p>Асинхронный запрос на загрузку данных гистограммы.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>лоадтекстурефромфилеасинк</strong></a></td><td style="text-align: left;"><p>Загружает текстуру из файла и уведомляет узел асинхронно по завершении.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>лоадтекстуреслицеасинк</strong></a></td><td style="text-align: left;"><p>Загружает срез текстуры и уведомляет асинчрнаусли узла о завершении.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>реадтекселвалуеасинк</strong></a></td><td style="text-align: left;"><p>Считывает значение шаг текселя и возвращает результат в асинчрнаусли узла.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>рендертекстуреасинк</strong></a></td><td style="text-align: left;"><p>Визуализирует текстуру в файл и возвращает результат в асинчрнаусли узла.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>саветекстуреасинк</strong></a></td><td style="text-align: left;"><p>Сохраняет текстуру.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 
