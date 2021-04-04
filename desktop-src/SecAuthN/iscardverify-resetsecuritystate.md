---
description: Сбрасывает текущий контекст безопасности смарт-карты.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'Метод Искардверифи:: Ресетсекуритистате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896746"
---
# <a name="iscardverifyresetsecuritystate-method"></a>Метод Искардверифи:: Ресетсекуритистате

\[Метод **ресетсекуритистате** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **ресетсекуритистате** Сбрасывает текущий [*контекст безопасности*](../secgloss/s-gly.md) [*смарт-карты*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений:



| Код возврата                                                                                   | Описание                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                    |



 

## <a name="remarks"></a>Комментарии

Чтобы повторно включить [*контекст безопасности*](../secgloss/s-gly.md) без сброса параметров, вызовите метод [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардверифи**](iscardverify.md).

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

[**искардверифи**](iscardverify.md)
</dt> <dt>

[**Внести**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))
</dt> </dl>

 

 
