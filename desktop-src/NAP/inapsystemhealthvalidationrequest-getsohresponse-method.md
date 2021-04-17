---
title: Метод Инапсистемхеалсвалидатионрекуест Жетсохреспонсе (Напсистемхеалсвалидатор. h)
description: Извлекает Сохреспонсе.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Метод Жетсохреспонсе NAP
- Метод Жетсохреспонсе NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Жетсохреспонсе
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672853"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a>Метод Инапсистемхеалсвалидатионрекуест:: Жетсохреспонсе

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапсистемхеалсвалидатионрекуест:: жетсохреспонсе** извлекает [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сохреспонсе* \[ заполняет\]
</dt> <dd>

Указатель на указатель на полученный [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh).

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
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Напсистемхеалсвалидатор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напсистемхеалсвалидатор. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инапсистемхеалсвалидатионрекуест**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





