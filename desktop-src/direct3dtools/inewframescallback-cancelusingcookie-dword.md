---
description: Обратный вызов, уведомляющий узел об отмене запроса с помощью файла cookie, уникально идентифицирующего запрос.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иневфрамескаллбакк:: Канцелусингкукие'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494715"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>Метод Иневфрамескаллбакк:: Канцелусингкукие

Обратный вызов, уведомляющий узел об отмене запроса с помощью файла cookie, уникально идентифицирующего запрос.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a>Параметры

*рекуесткукие*   
Файл cookie, который уникальным образом иденфиес отмененный запрос.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иневфрамескаллбакк**](/windows/desktop/direct3dtools/inewframescallback)

 

 
