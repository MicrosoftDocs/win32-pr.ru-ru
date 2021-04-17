---
title: Функция Вмдрмшутдовн (Вмдрмсдк. h)
description: Функция Вмдрмшутдовн освобождает ресурсы, используемые расширенными API-интерфейсами клиента DRM Windows Media.
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
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674891"
---
# <a name="wmdrmshutdown-function"></a>Функция Вмдрмшутдовн

Функция **вмдрмшутдовн** освобождает ресурсы, используемые расширенными API-интерфейсами клиента DRM Windows Media.

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



 

## <a name="remarks"></a>Комментарии

Чтобы избежать утечек памяти, необходимо вызвать эту функцию для каждого вызова функции [**вмдрмстартуп**](wmdrmstartup.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции**](drm-functions.md)
</dt> </dl>

 

 





