---
title: Метод Ивмдрмлиценсе CreateDecryptor (Вмдрмсдк. h)
description: Метод CreateDecryptor создает объект дешифратора, используя параметры текущей лицензии.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Формат Windows Media, CreateDecryptor метод
- CreateDecryptor метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ac7e6bb1e9d4f9e5e7c706c0a9e3518f62b1068ed743dc795554dd43ac61e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027712"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>Метод Ивмдрмлиценсе:: CreateDecryptor

Метод **CreateDecryptor** создает объект дешифратора, используя параметры текущей лицензии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдекриптор* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**ивмдрмдекрипт**](iwmdrmdecrypt.md) только что созданного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                | Описание                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt> </dl> | Требуется обновленный список отзыва содержимого.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>                       | Метод выполнен успешно.<br/>                         |



 

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**креатинкриптор**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**Интерфейс Ивмдрмлиценсе**](iwmdrmlicense.md)
</dt> </dl>

 

 





