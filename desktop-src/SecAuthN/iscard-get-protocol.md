---
description: Возвращает идентификатор протокола, используемого в данный момент на смарт-карте.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: Метод get_Protocol. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f59522f9ec5f22976874aff225d73fc44e8e0cfa8f06022e22312ab8bd80858
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482164"
---
# <a name="iscardget_protocol-method"></a>Метод "карточки:: получение \_ протокола"

\[Метод **Get \_ Protocol** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **получения \_ протокола** получает идентификатор протокола, используемого на [*смарт-карте*](../secgloss/s-gly.md)в настоящий момент.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппротокол* \[ заполняет\]
</dt> <dd>

Указатель на идентификатор протокола.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Operation completed successfully (Операция выполнена успешно).<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *ппротокол* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>    | В *ппротокол* был передан неверный указатель.<br/> |



 

## <a name="remarks"></a>Remarks

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как получить идентификатор протокола, используемого на смарт-карте в данный момент.


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
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

[**получить \_ контекст**](iscard-get-context.md)
</dt> <dt>

[**получение \_ состояния**](iscard-get-status.md)
</dt> <dt>

[**Карточка**](iscard.md)
</dt> </dl>

 

 
