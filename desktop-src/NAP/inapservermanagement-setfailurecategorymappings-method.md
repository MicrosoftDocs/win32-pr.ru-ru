---
title: Метод Инапсерверманажемент Сетфаилурекатегоримаппингс (Напсерверманажемент. h)
description: Используется для задания сопоставлений категорий сбоев SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Метод Сетфаилурекатегоримаппингс NAP
- Метод Сетфаилурекатегоримаппингс NAP, интерфейс Инапсерверманажемент
- Инапсерверманажемент интерфейса NAP, метод Сетфаилурекатегоримаппингс
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988955"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a>Метод Инапсерверманажемент:: Сетфаилурекатегоримаппингс

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапсерверманажемент:: сетфаилурекатегоримаппингс** используется для задания сопоставлений категорий сбоев SHV.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор* \[ в\]
</dt> <dd>

Объект [**системхеалсентитид**](nap-type-constants.md) , содержащий уникальный идентификатор SHV.

</dd> <dt>

*сопоставление* \[ окне\]
</dt> <dd>

Структура [**фаилурекатегоримаппинг**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) , содержащая данные сопоставления категорий сбоев.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                     | Описание                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>           | Операция успешно завершена.<br/>                                    |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl> | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>  | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Напсерверманажемент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсерверманажемент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инапсерверманажемент**](inapservermanagement.md)
</dt> </dl>

 

 





