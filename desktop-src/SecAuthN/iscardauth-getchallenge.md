---
description: Метод метода WebMethod возвращает запрос со смарт-карты.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'Метод Искардаус:: Challenge'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263588"
---
# <a name="iscardauthgetchallenge-method"></a>Метод Искардаус:: Challenge

\[Метод **метода** WebMethod доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **метода WebMethod возвращает запрос со** [*смарт-карты*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лалгоид* \[ в необязательное\]
</dt> <dd>

Алгоритм, используемый в процессе проверки подлинности.

</dd> <dt>

*лленгсофчалленже* \[ окне\]
</dt> <dd>

Максимальная длина ожидаемого ответа.

</dd> <dt>

*ппарам* \[ окне\]
</dt> <dd>

Объект [**ибитебуффер**](ibytebuffer.md) , содержащий зависящие от поставщика параметры процесса проверки подлинности.

</dd> <dt>

*pBuffer* \[ в, out\]
</dt> <dd>

На входе указывает на буфер.

На выходе содержит данные запроса из карточки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Передан неверный указатель.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                    |



 

## <a name="remarks"></a>Комментарии

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардаус**](iscardauth.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардаус**](iscardauth.md)
</dt> </dl>

 

 
