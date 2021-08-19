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
ms.openlocfilehash: c369be95314ceaf3c4babce9dacd962fd3391d4f39f8988ef56f51fb3133aee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027592"
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



 

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмдрмлиценсеманажемент**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





