---
title: Метод INapEnforcementClientConnection2 Жетинсталледшвс (Напенфорцементклиент. h)
description: Используется агентом NAP для запроса установленных средств проверки работоспособности системы (SHV) на клиенте.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Метод Жетинсталледшвс NAP
- Метод Жетинсталледшвс NAP, интерфейс INapEnforcementClientConnection2
- INapEnforcementClientConnection2 интерфейса NAP, метод Жетинсталледшвс
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493248"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>Метод INapEnforcementClientConnection2:: Жетинсталледшвс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **жетинсталледшвс** используется агентом NAP для запроса установленных средств проверки работоспособности системы (SHV) на клиенте.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*количество* \[ заполняет\]
</dt> <dd>

Указатель на значение [системхеалсентитикаунт](nap-datatypes.md) , указывающее число установленных SHV в *идентификаторах*.

</dd> <dt>

*идентификаторы* \[ заполняет\]
</dt> <dd>

Указатель на массив значений [системхеалсентитид](nap-datatypes.md) , содержащих установленные идентификаторы SHV.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                   | Описание                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>         | Операция успешно завершена.<br/>                          |
| <dl> <dt>**Д \_ INVALIDARG**</dt> </dl> | Методу передан недопустимый аргумент.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





