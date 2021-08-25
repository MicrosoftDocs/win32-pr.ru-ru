---
description: Обратный вызов, уведомляющий узел о ходе выполнения связанного запроса.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ипикспрогресскаллбакк: метод:P рогресс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0bcf3ce7e443d2fb7964f07effdac8648edc652c48c8110fa8574bd62e3d9a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845324"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>Ипикспрогресскаллбакк: метод:P рогресс

Обратный вызов, уведомляющий узел о ходе выполнения связанного запроса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a>Параметры

*данном*   
Часть запроса завершена в виде количества завершенных шагов.

*maxSize*   
Общее число шагов для выполнения запроса.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипикспрогресскаллбакк**](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
