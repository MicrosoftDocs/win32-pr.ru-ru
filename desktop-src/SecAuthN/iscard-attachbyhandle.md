---
description: Присоединяет объект открытк к открытому и настроенному обработчику смарт-карты.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: Метод Аттачбихандле (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647616"
---
# <a name="iscardattachbyhandle-method"></a>Метод Аттачбихандле::

\[Метод **аттачбихандле** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **аттачбихандле** Присоединяет объект [**кредитной карты**](iscard.md) к открытому и настроенному обработчику [*смарт-карты*](../secgloss/s-gly.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хкард* \[ окне\]
</dt> <dd>

Маркер открытого соединения со смарт-картой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Operation completed successfully (Операция выполнена успешно).<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *хкард* .<br/> |



 

## <a name="remarks"></a>Комментарии

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

Завершив использование этого маркера, отпустите вложение, вызвав метод [**етач::D**](iscard-detach.md) .

## <a name="examples"></a>Примеры

В следующем примере показано подключение к обработчику смарт-карты.


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
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

[**аттачбиреадер**](iscard-attachbyreader.md)
</dt> <dt>

[**Соединил**](iscard-detach.md)
</dt> <dt>

[**получить \_ кардхандле**](iscard-get-cardhandle.md)
</dt> <dt>

[**Карточка**](iscard.md)
</dt> <dt>

[**Повторно подключиться**](iscard-reattach.md)
</dt> </dl>

 

 
