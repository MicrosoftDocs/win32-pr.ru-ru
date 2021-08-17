---
description: Задает новый ответ КАТЕГОРИЯХ APDU.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: 'Искардкмд: метод ut_ApduReply:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 749c0aee678a036160b52db635f2f096c68e0d20b2295c05387c5b57bbe2befc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481464"
---
# <a name="iscardcmdput_apdureply-method"></a>Искардкмд::p UT \_ апдурепли метод

\[Метод **размещения \_ апдурепли** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **размещения \_ апдурепли** ЗАДАЕТ новый [*ответ категориях APDU*](../secgloss/r-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*препляпду* \[ окне\]
</dt> <dd>

Указатель на буфер байтов (сопоставляется через объект **IStream** ), который содержит сообщение категориях APDU воспроизведения для возврата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *препляпду* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *препляпду* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                            |



 

## <a name="remarks"></a>Remarks

Чтобы получить существующий ответ КАТЕГОРИЯХ APDU, вызовите [**Get \_ апдурепли**](iscardcmd-get-apdureply.md).

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как задать новый [*ответ категориях APDU*](../secgloss/r-gly.md). В примере предполагается, что Пибитерепли является допустимым указателем на экземпляр [**ибитебуффер**](ibytebuffer.md), а пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
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

[**получить \_ апдурепли**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**получить \_ апдуреплиленгс**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
