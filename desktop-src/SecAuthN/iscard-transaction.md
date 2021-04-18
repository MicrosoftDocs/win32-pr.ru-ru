---
description: Выполняет операцию записи и чтения для объекта команды смарт-карты (блок данных протокола приложения).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: Метод "Скардмгр. h"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650630"
---
# <a name="iscardtransaction-method"></a>Метод "a Card:: Transaction"

\[Метод **Transaction** доступен для использования в операционных системах, указанных в разделе требования. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Transaction** выполняет операцию записи и чтения для команды [*смарт-карты*](../secgloss/s-gly.md) ([*блок данных протокола приложения*](../secgloss/a-gly.md)). Строка ответа смарт-карты для строки команды, определенной в карточке, отправленной на смарт-карту, будет доступна после возврата этой функции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппкмд* \[ в, out\]
</dt> <dd>

Указатель на объект команды смарт-карты.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Операция выполнена успешно.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *ппкмд* .<br/>           |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *ппкмд* был передан неверный указатель.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Память для удовлетворения запроса недоступна.<br/> |



 

## <a name="remarks"></a>Комментарии

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано выполнение операции записи и чтения для объекта команды смарт-карты.


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Скардмгр. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардмгр. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аттачбихандле**](iscard-attachbyhandle.md)
</dt> <dt>

[**аттачбиреадер**](iscard-attachbyreader.md)
</dt> <dt>

[**Соединил**](iscard-detach.md)
</dt> <dt>

[**получение \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**получить \_ кардхандле**](iscard-get-cardhandle.md)
</dt> <dt>

[**получить \_ контекст**](iscard-get-context.md)
</dt> <dt>

[**получить \_ протокол**](iscard-get-protocol.md)
</dt> <dt>

[**получение \_ состояния**](iscard-get-status.md)
</dt> <dt>

[**Карточка**](iscard.md)
</dt> <dt>

[**локкскард**](iscard-lockscard.md)
</dt> <dt>

[**Повторно подключиться**](iscard-reattach.md)
</dt> <dt>

[**унлоккскард**](iscard-unlockscard.md)
</dt> </dl>

 

 
