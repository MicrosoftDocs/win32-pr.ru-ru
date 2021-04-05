---
title: Метод Validate Инапсохконструктор (Наппротокол. h)
description: Проверяет допустимость пакета SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Проверка метода NAP
- Проверка метода NAP, интерфейс Инапсохконструктор
- Инапсохконструктор интерфейса NAP, метод Validate
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803106"
---
# <a name="inapsohconstructorvalidate-method"></a>Метод Инапсохконструктор:: Validate

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапсохконструктор:: Validate** проверяет допустимость пакета SoH.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состояние работоспособности* \[ окне\]
</dt> <dd>

Указатель на сконструированный пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*запрос* \[ окне\]
</dt> <dd>

**Логическое** **значение** , равное true, если пакет является [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , и **false** , если это **сохреспонсе**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                            | Описание                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>                  | Пакет SoH является допустимым.<br/>                                |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl>        | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>         | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |
| <dl> <dt>**\_ \_ Недопустимый \_ пакет NAP E**</dt> </dl> | Недопустимый пакет SoH.<br/>                              |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Наппротокол. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Наппротокол. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инапсохконструктор**](inapsohconstructor.md)
</dt> </dl>

 

 





