---
description: Извлекает маркер подключенной смарт-карты. Этот метод возвращает ( \* фандле) = = null, если соединение отсутствует.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: Метод get_CardHandle. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8a01b7c4531b82c154b6c6e04c1cf0fb5fa2003729e8abf5c0af39470a171bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482234"
---
# <a name="iscardget_cardhandle-method"></a>Метод кардхандле:: Get \_

\[Метод **Get \_ кардхандле** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Get \_ кардхандле** Извлекает маркер подключенной [*смарт-карты*](../secgloss/s-gly.md). Этот метод возвращает ( \* фандле) = = **null** , если соединение отсутствует.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фандле* \[ заполняет\]
</dt> <dd>

Указатель на маркер карты при возврате.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Operation completed successfully (Операция выполнена успешно).<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *фандле* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>    | В *фандле* был передан неверный указатель.<br/> |



 

## <a name="remarks"></a>Remarks

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано получение маркера смарт-карты.


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Скардмгр. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардмгр. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**получение \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**получить \_ контекст**](iscard-get-context.md)
</dt> <dt>

[**получить \_ протокол**](iscard-get-protocol.md)
</dt> <dt>

[**получение \_ состояния**](iscard-get-status.md)
</dt> <dt>

[**Карточка**](iscard.md)
</dt> </dl>

 

 
