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
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910355"
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
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Нет</dt> </dl>        |
| Библиотека<br/>                  | <dl> <dt>Ртворкк. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
