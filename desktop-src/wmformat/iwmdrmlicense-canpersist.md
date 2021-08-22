---
title: Метод Ивмдрмлиценсе Канперсист (Вмдрмсдк. h)
description: Метод Канперсист запрашивает возможность сохранения лицензии в локальном хранилище лицензий.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Формат Windows Media, Канперсист метод
- Канперсист метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Канперсист
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e174f0b7d48684e40cc5796d2ae95ec1bcaca99216c493c73609323daf276b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701222"
---
# <a name="iwmdrmlicensecanpersist-method"></a>Метод Ивмдрмлиценсе:: Канперсист

Метод **канперсист** запрашивает возможность сохранения лицензии в локальном хранилище лицензий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфканперсист* \[ заполняет\]
</dt> <dd>

Значение TRUE указывает, что лицензия может быть сохранена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмлиценсе**](iwmdrmlicense.md)
</dt> </dl>

 

 





