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
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672867"
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



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                               |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Напсистемхеалсвалидатор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсистемхеалсвалидатор. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





