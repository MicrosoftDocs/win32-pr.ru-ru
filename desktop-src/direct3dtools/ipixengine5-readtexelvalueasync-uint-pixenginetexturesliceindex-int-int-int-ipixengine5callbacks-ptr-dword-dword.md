---
description: Считывает значение шаг текселя и возвращает результат в асинчрнаусли узла.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Реадтекселвалуеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d81427e7305d8bf7abee3897705cf7074825b1993deacbd04c5e454235a520b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022534"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Реадтекселвалуеасинк

Считывает значение шаг текселя и возвращает результат в асинчрнаусли узла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*текстуреид*   
Идентификатор текстуры, из которой считывается значение шаг текселя.

*слицеиндекс*   
Индекс среза в текстуре, из которого считывается значение шаг текселя.

*x*   
Координата x шаг текселя для чтения.

*&*   
Координата y шаг текселя для чтения.

*форматоверриде*   
Переопределение формата цвета.

*обратные вызовы*   
Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.

*рекуесткукие*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

*прогрессинтервалмсекс*   
Не используется.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
