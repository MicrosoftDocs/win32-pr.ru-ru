---
description: Извлекает текущий маркер контекста диспетчера ресурсов. Этот метод возвращает ( \* пконтекст) = = null, если контекст не был установлен.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: Метод get_Context. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 82094d51912031655585cacde0b156451107276bc08ca1be6dc6d82bdbb3229d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015634"
---
# <a name="iscardget_context-method"></a>Метод "карточки:: получение \_ контекста"

\[Метод **Get \_ context** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **получения \_ контекста** получает текущий маркер [*контекста диспетчера ресурсов*](../secgloss/r-gly.md) . Этот метод возвращает ( \* *пконтекст*) = = **null** , если контекст не был установлен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекст* \[ заполняет\]
</dt> <dd>

Указатель на маркер контекста при возврате.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Operation completed successfully (Операция выполнена успешно).<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *пконтекст* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>    | В *пконтекст* был передан неверный указатель.<br/> |



 

## <a name="remarks"></a>Remarks

Контекст Resource Manager задается путем вызова функции [*смарт-карты*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано извлечение текущего маркера [*контекста диспетчера ресурсов*](../secgloss/r-gly.md) .


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
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

[**получить \_ кардхандле**](iscard-get-cardhandle.md)
</dt> <dt>

[**получить \_ протокол**](iscard-get-protocol.md)
</dt> <dt>

[**получение \_ состояния**](iscard-get-status.md)
</dt> <dt>

[**Карточка**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
