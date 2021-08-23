---
description: Задает заданный идентификатор инструкции в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: 'Искардкмд: метод ut_InstructionId:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7c9c5653bb4d6832161f313b924ba5c1a4f3d80c89ead48f19439935b534b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577364"
---
# <a name="iscardcmdput_instructionid-method"></a>Искардкмд::p UT \_ инструктионид метод

\[Метод **размещения \_ инструктионид** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **размещения \_ инструктионид** задает заданный идентификатор инструкции в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Бинс* \[ окне\]
</dt> <dd>

Байт, который является идентификатором инструкции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *Бинс* .<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                      |



 

## <a name="remarks"></a>Remarks

Чтобы получить существующий идентификатор инструкции, вызовите [**Get \_ инструктионид**](iscardcmd-get-instructionid.md).

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как задать идентификатор инструкции в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU). В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
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

[**получить \_ инструктионид**](iscardcmd-get-instructionid.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
