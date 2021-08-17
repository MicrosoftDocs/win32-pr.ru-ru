---
title: Функция Вмдрмшутдовн (Вмдрмсдк. h)
description: функция вмдрмшутдовн высвобождает ресурсы, используемые расширенными api клиента DRM для Windows Media.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Вмдрмшутдовн функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80f0f7264cd0962cb642f0877ccd044e777c3e9f269f87fcffc0037dcc0836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930373"
---
# <a name="wmdrmshutdown-function"></a>Функция Вмдрмшутдовн

функция **вмдрмшутдовн** высвобождает ресурсы, используемые расширенными api клиента DRM для Windows Media.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Чтобы избежать утечек памяти, необходимо вызвать эту функцию для каждого вызова функции [**вмдрмстартуп**](wmdrmstartup.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции**](drm-functions.md)
</dt> </dl>

 

 





