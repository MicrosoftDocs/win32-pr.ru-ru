---
description: Запросы на получение содержимого мозаичной текстуры в виде. Файл DDS (поверхность DirectDraw).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Итилерекуест:: Рекуесттекстуретилеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140126"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>Метод Итилерекуест:: Рекуесттекстуретилеасинк

Запросы на получение содержимого мозаичной текстуры в виде. Файл DDS (поверхность DirectDraw).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>Параметры

*1008*   
Указанное событие для сопоставления содержимого буфера с (например, целевой объект прорисовки может измениться со временем).

*текстурефилептр*   
Адрес указанного объекта текстуры.

*тилесубресаурце*   
Указанный подресурс плитки.

*тилекс*   
Указанная Координата X плитки.

*Плитка*   
Указанная координата плитки Y.

*тилез*   
Заданная Координата на плитке Z.

*ддсфиленаме*   
Строка COM, содержащая путь к DDS-файлу, в который записываются результаты.

*прекуесткаллбакк*   
Адрес обратного вызова, используемый для уведомления узла о результатах.

*рекуесткукие*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

*прогрессинтервалмсекс*   
Не используется.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**итилерекуест**](/windows/desktop/direct3dtools/itilerequest)

 

 
