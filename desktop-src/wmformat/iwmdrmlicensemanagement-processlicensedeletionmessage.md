---
title: Метод Ивмдрмлиценсеманажемент Процесслиценседелетионмессаже (Вмдрмсдк. h)
description: Метод Процесслиценседелетион удаляет лицензию, которая была импортирована для содержимого, изначально защищенного с помощью другой системы защиты содержимого.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Формат Windows Media, Процесслиценседелетионмессаже метод
- Процесслиценседелетионмессаже метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Процесслиценседелетионмессаже
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717902"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>Ивмдрмлиценсеманажемент: метод:P Роцесслиценседелетионмессаже

Метод **процесслиценседелетион** удаляет лицензию, которая была импортирована для содержимого, изначально защищенного с помощью другой системы защиты содержимого.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрделетионмессаже* \[ окне\]
</dt> <dd>

Сообщение, идентифицирующее удаляемую лицензию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмлиценсеманажемент**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





