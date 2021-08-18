---
description: Указывает адрес узла (NAD) для использования с интерфейсом Искардкмд.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'Искардкмд: метод ut_Nad:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 84ade2e2ca69c328650f4c7df485814e4eaacedf3fdb0190fc883cde864a8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481394"
---
# <a name="iscardcmdput_nad-method"></a>Искардкмд::p \_ метод UT NAD

\[Метод **размещения \_ NAD** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **размещения \_ NAD** указывает адрес узла (NAD) для использования с интерфейсом [**искардкмд**](iscardcmd.md) . Это относится только к обмену данными по [*протоколу T = 1*](../secgloss/t-gly.md) . По умолчанию объект [**искардкмд**](iscardcmd.md) использует значение NAD, равное нулю.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бнад* \[ окне\]
</dt> <dd>

Байт, представляющий используемую NAD.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Операция успешно завершена.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *бнад* .<br/>    |



 

## <a name="remarks"></a>Remarks

Этот метод следует вызывать только в том случае, если для NAD необходимо использовать значение, отличное от нуля.

## <a name="examples"></a>Примеры

В следующем примере показано, как указать адрес узла для использования с интерфейсом [**искардкмд**](iscardcmd.md) . В примере предполагается, что Бинадвалуе является переменной типа **Byte** , которой ранее было присвоено значение, а пискардкмд является допустимым указателем на экземпляр интерфейса **искардкмд** .


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
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
| Header<br/>                   | <dl> <dt>Скарддат. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скарддат. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
