---
title: Метод Инапклиентманажемент Жетнапклиентинфо (Напманажемент. h)
description: Извлекает сведения о клиенте NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Метод Жетнапклиентинфо NAP
- Метод Жетнапклиентинфо NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Жетнапклиентинфо
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534631"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a>Метод Инапклиентманажемент:: Жетнапклиентинфо

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **жетнапклиентинфо** извлекает сведения о клиенте NAP.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*иснапенаблед* \[ заполняет\]
</dt> <dd>

Указатель на логическое значение **true** , если включен NAP. в противном случае — значение **false**.

</dd> <dt>

*clientName* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую имя клиента.

</dd> <dt>

*клиентдескриптион* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую описание клиента.

</dd> <dt>

*протоколверсион* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую версию протокола.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.



| Код возврата                                                                                         | Описание                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                | Операция выполнена успешно.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |
| <dl> <dt>**RPC \_ E \_ отключен**</dt> </dl> | Напажент не работает.<br/>                            |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Напманажемент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напманажемент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инапклиентманажемент**](inapclientmanagement.md)
</dt> </dl>

 

 





