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
ms.openlocfilehash: 40cb18f749adc9a1b7003a777cc821fb5e003b83322a7d54c2efda4b8e5739f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939645"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Напенфорцементклиент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напенфорцементклиент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





