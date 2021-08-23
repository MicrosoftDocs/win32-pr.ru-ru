---
title: Метод INapSystemHealthValidationRequest2 Жетконфигид (Напсистемхеалсвалидатор. h)
description: Используется средствами проверки работоспособности системы (SHV) для получения идентификатора конфигурации в запросе на проверку.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Метод Жетконфигид NAP
- Метод Жетконфигид NAP, интерфейс INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 интерфейса NAP, метод Жетконфигид
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72acdd170726d2d94e4fbc46864a7e5aab6b902d7b1ee25b63ee0fa9e376c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625984"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>Метод INapSystemHealthValidationRequest2:: Жетконфигид

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **INapSystemHealthValidationRequest2:: жетконфигид** используется средствами проверки работоспособности системы (SHV) для получения идентификатора конфигурации в запросе на проверку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*конфигид* \[ заполняет\]
</dt> <dd>

При возвращении — указатель на UINT32, содержащий идентификатор конфигурации SHV.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.



| Код возврата                                                                                  | Описание                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Операция выполнена успешно.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Параметр Конфигид имеет **значение NULL**.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                               |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Напсистемхеалсвалидатор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсистемхеалсвалидатор. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>См. также

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





