---
description: Завершает асинхронный запрос на отмену регистрации рабочей очереди с помощью задачи службы планировщика классов мультимедиа (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Функция Ртвкендунрегистерворккуеуевисммксс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: 083f0ca787bb842850320b9dd1d320ef4d5b172ee0b6d9b117296e58b991bd0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793404"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>Функция Ртвкендунрегистерворккуеуевисммксс

Завершает асинхронный запрос на отмену регистрации рабочей очереди с помощью задачи службы планировщика классов мультимедиа (MMCSS).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пресулт* 
</dt> <dd>

Указатель на интерфейс [**имфасинкресулт**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) . Передайте тот же указатель, который был получен объектом обратного вызова в методе [**иртвкасинккаллбакк:: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>None</dt> </dl>        |
| Библиотека<br/>                  | <dl> <dt>Ртворкк. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
