---
description: Функция обратного вызова, используемая для уведомления узла об ошибках во время записи или воспроизведения.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифилеиокаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f1adc4fdc72cd26e317a2d8dc4a82049a2ef6ad99734d5e8bfc631bffdf4df99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981524"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>Метод Ифилеиокаллбакк:: Ресулткаллбакк

Функция обратного вызова, используемая для уведомления узла об ошибках во время записи или воспроизведения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a>Параметры

*ресултстате*   
Указывает тип обнаруженной ошибки.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ифилеиокаллбакк**](/windows/desktop/direct3dtools/ifileiocallback)

 

 
