---
description: Обратный вызов, уведомляющий узел о буфера кадров данных, возвращаемых связанным запросом.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамебуфферкаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2308ec5355da8f8fda7eeccf31d1cbe19e8a8247
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626680"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Метод Ифрамебуфферкаллбакк:: Ресулткаллбакк

Обратный вызов, уведомляющий узел о буфера кадров данных, возвращаемых связанным запросом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a>Параметры

*фраменумбер*   
Номер кадра.

*Ширина*   
Ширина рамки.

*равно*   
Высота рамки.

*рендертаржетптр*   
Целевой объект отрисовки, из которого берутся результаты. Он всегда является слотом, заданным запросом буфера кадров, или, если не вызовом Draw, первый РТВ баунт в источник вывода.

*фрамедурактион*   
Не используется.

*изменять*   
Размер выходного буфера в байтах.

*\_буфер count5*   
Содержимое целевого объекта отрисовки в формате R8G8B8A8 \_ UNORM.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ифрамебуфферкаллбакк**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
