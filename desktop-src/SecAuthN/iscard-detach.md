---
description: Закрывает открытое подключение к смарт-карте.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: A-карта::D метод етач (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647614"
---
# <a name="iscarddetach-method"></a>Етач: метод:D

\[Метод **Detach** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Detach** закрывает открытое подключение к [*смарт-карте*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расстановка* \[ окне\]
</dt> <dd>

Указывает, что следует делать с картой в подключенном [*модуле чтения*](../secgloss/r-gly.md).



| Значение                                                                                                                                      | Значение                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**ВЫХОДА**</dt> </dl>       | Оставляет смарт-карту в текущем [*состоянии*](../secgloss/s-gly.md).<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**ПЕРЕЗАПУСК**</dt> </dl>       | Сбрасывает смарт-карту в известное состояние.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**Непитание**</dt> </dl> | Удаляет электроэнергию смарт-карты.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**ВЫДВИНУТ**</dt> </dl>       | Извлекает смарт-карту, если у читателя есть возможности извлечения.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Operation completed successfully (Операция выполнена успешно).<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимое *Расположение* .<br/>       |



 

## <a name="remarks"></a>Комментарии

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано закрытие подключения к смарт-карте.


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
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

[**Карточка**](iscard.md)
</dt> <dt>

[**Повторно подключиться**](iscard-reattach.md)
</dt> </dl>

 

 
