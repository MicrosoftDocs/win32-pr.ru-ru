---
title: Метод Ивмдрмлиценсе Креатинкриптор (Вмдрмсдк. h)
description: Метод Креатинкриптор создает объект шифратора, используя параметры текущей лицензии.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Формат Windows Media, Креатинкриптор метод
- Креатинкриптор метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Креатинкриптор
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704476"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>Метод Ивмдрмлиценсе:: Креатинкриптор

Метод **креатинкриптор** создает объект шифратора, используя параметры текущей лицензии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенкриптор* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**ивмдрменкрипт**](iwmdrmencrypt.md) только что созданного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                | Описание                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt> </dl> | Требуется обновленный список отзыва содержимого.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>                       | Метод выполнен успешно.<br/>                         |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**Интерфейс Ивмдрмлиценсе**](iwmdrmlicense.md)
</dt> </dl>

 

 





