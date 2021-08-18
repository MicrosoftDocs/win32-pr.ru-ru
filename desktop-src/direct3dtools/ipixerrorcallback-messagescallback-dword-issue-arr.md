---
description: Обратный вызов, уведомляющий узел о сообщениях, возвращенных связанным запросом.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиксерроркаллбакк:: Мессажескаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dc3ac06652c76838f246df006fbea78430979761ed92cf63bda0d6cf6c141ff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985884"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>Метод Ипиксерроркаллбакк:: Мессажескаллбакк

Обратный вызов, уведомляющий узел о сообщениях, возвращенных связанным запросом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a>Параметры

*расчета*   
Число сообщений.

*\_сообщения count0*   
Сообщения.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипиксерроркаллбакк**](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
