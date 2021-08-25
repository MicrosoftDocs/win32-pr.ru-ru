---
title: Функция Вмдрмстартуп (Вмдрмсдк. h)
description: функция вмдрмстартуп инициализирует ресурсы, используемые расширенными api клиента DRM для Windows Media.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Вмдрмстартуп функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c194a8c060ad1626fde796510c25c83e3e163dafffe9c17df17a7dcec890be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928748"
---
# <a name="wmdrmstartup-function"></a>Функция Вмдрмстартуп

функция **вмдрмстартуп** инициализирует ресурсы, используемые расширенными api клиента DRM для Windows Media.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Для каждого вызова этой функции необходимо вызвать [**вмдрмшутдовн**](wmdrmshutdown.md) , чтобы освободить используемые ресурсы.

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

 

 





