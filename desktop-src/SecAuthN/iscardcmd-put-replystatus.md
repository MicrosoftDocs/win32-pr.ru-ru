---
description: Задает новое слово состояния ответного сообщения КАТЕГОРИЯХ APDU.
ms.assetid: 17b498eb-2268-451a-9f5c-c53cb7e42019
title: 'Искардкмд: метод ut_ReplyStatus:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ff4f7ffeddd94a3c4e68f7a343c9936d8e360594898f2811575e7a1067030161
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577314"
---
# <a name="iscardcmdput_replystatus-method"></a>Искардкмд::p UT \_ реплистатус метод

\[Метод **размещения \_ реплистатус** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **постановки \_ реплистатус** задает новое слово состояния [*ответного сообщения категориях APDU*](../secgloss/r-gly.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ReplyStatus(
  [in] WORD wStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*встатус* \[ окне\]
</dt> <dd>

Слово, которое является состоянием.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *встатус* .<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                        |



 

## <a name="remarks"></a>Remarks

Чтобы получить слово состояния сообщения ответа КАТЕГОРИЯХ APDU, вызовите [**Get \_ реплистатус**](iscardcmd-get-replystatus.md).

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как задать новое сообщение о состоянии [*ответа категориях APDU*](../secgloss/r-gly.md) . В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
WORD     wNewStatus = 0x0000;
HRESULT  hr;

// Set reply status.
hr = pISCardCmd->put_ReplyStatus(wNewStatus);
if (FAILED(hr))
{
  printf("Failed put_ReplyStatus\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Скарддат. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скарддат. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**получить \_ реплистатус**](iscardcmd-get-replystatus.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
