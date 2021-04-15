---
description: Создает канал связи с модулем чтения, используя предоставляемое отображаемое имя для модуля чтения.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Метод Искардманаже:: Аттачбифд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647435"
---
# <a name="iscardmanageattachbyifd-method"></a>Метод Искардманаже:: Аттачбифд

\[Метод **аттачбифд** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **аттачбифд** создает канал связи с [*модулем чтения*](../secgloss/r-gly.md), используя предоставляемое отображаемое имя для модуля чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрифднаме* \[ окне\]
</dt> <dd>

Отображаемое имя модуля чтения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений:



| Код возврата                                                                                   | Описание                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *бстрифднаме* .<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                            |



 

## <a name="remarks"></a>Комментарии

Для подключения [**аттачбихандле**](iscardmanage-attachbyhandle.md)вызова [*смарт-карты*](../secgloss/s-gly.md) .

Освобождение вызова [**отсоединения**](iscardmanage-detach.md)вложений.

Чтобы повторно подключиться к смарт-карте, не вызывая [**Detach**](iscardmanage-detach.md) и **аттачбифд**, вызовите [**Reconnect**](iscardmanage-reconnect.md).

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).

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

[**аттачбихандле**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**Соединил**](iscardmanage-detach.md)
</dt> <dt>

[**искардманаже**](iscardmanage.md)
</dt> <dt>

[**Повтор соединения**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
