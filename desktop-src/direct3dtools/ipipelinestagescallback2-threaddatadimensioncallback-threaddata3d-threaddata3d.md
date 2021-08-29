---
description: Обратный вызов, уведомляющий узел о количестве потоков и групп шейдера вычислений в связанном запросе.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesCallback2:: Среаддатадименсионкаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c96de717cbe9632c2b2fa610ef8e1c6aefcf6bf
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623790"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>Метод IPipeLineStagesCallback2:: Среаддатадименсионкаллбакк

Обратный вызов, уведомляющий узел о количестве потоков и групп шейдера вычислений в связанном запросе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a>Параметры

*среадграупкаунт*   
Многомерное число групп потоков.

*среадграупсизе*   
Многомерный размер каждой группы потоков.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPipeLineStagesCallback2**](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
