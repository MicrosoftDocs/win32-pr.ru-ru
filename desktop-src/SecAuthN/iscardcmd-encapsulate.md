---
description: Метод инкапсуляции инкапсулирует заданную единицу данных протокола приложения командной строки (КАТЕГОРИЯХ APDU) в другую команду КАТЕГОРИЯХ APDU для передачи на смарт-карту.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'Метод Искардкмд:: инкапсулировать (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f531d0d5f55bea1fe63875a9feb508eb8b4c0e830705bfad2603cc52664c6f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015124"
---
# <a name="iscardcmdencapsulate-method"></a>Метод Искардкмд:: инкапсулировать

\[Метод **инкапсуляции** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **инкапсуляции** инкапсулирует заданную [*единицу данных протокола приложения*](../secgloss/a-gly.md) командной строки (категориях APDU) в другую команду категориях APDU для передачи на [*смарт-карту*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*папду* \[ окне\]
</dt> <dd>

Указатель на КАТЕГОРИЯХ APDU, который необходимо инкапсулировать.

</dd> <dt>

*Апдутипе* \[ окне\]
</dt> <dd>

ISO 7816-4. вариант [*T = 0*](../secgloss/t-gly.md) передач.

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

**ISO- \_ регистр \_ 1**
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

**ISO- \_ регистр \_ 2**
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

**\_Сценарий ISO \_ 3**
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

**ISO- \_ регистр \_ 4**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                   |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *папду* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                       |



 

## <a name="remarks"></a>Remarks

Чтобы создать команду КАТЕГОРИЯХ APDU, вызовите [**буилдкмд**](iscardcmd-buildcmd.md).

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как инкапсулировать команду КАТЕГОРИЯХ APDU. В примере предполагается, что Пибитеапду является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) .


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Требования



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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**буилдкмд**](iscardcmd-buildcmd.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
