---
title: Метод Инапсерверинфо Жетнапсерверинфо (Напсерверманажемент. h)
description: Извлекает сведения о сервере NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Метод Жетнапсерверинфо NAP
- Метод Жетнапсерверинфо NAP, интерфейс Инапсерверинфо
- Инапсерверинфо интерфейса NAP, метод Жетнапсерверинфо
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804066"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>Метод Инапсерверинфо:: Жетнапсерверинфо

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапсерверинфо:: жетнапсерверинфо** извлекает сведения о сервере NAP.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя сервера* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую имя сервера.

</dd> <dt>

*Описание* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую описание сервера.

</dd> <dt>

*протоколверсион* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую версию протокола.

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

[**инапсерверинфо**](inapserverinfo.md)
</dt> <dt>

[**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





