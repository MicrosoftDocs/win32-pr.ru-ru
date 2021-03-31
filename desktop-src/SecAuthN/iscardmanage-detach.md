---
description: Освобождает вложение на конкретную смарт-карту или модуль чтения, выделенный Аттачбихандле и Аттачбифд соответственно.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: 'Искардманаже: метод:D етач'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155499"
---
# <a name="iscardmanagedetach-method"></a>Искардманаже: метод:D етач

\[Метод **Detach** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Detach** освобождает вложение на конкретную [*смарт-карту*](../secgloss/s-gly.md) или [*модуль чтения*](../secgloss/r-gly.md) , выделенный [**аттачбихандле**](iscardmanage-attachbyhandle.md) и [**аттачбифд**](iscardmanage-attachbyifd.md) соответственно.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Detach();
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

Чтобы подключить смарт-карту, вызовите [**аттачбихандле**](iscardmanage-attachbyhandle.md) или [**аттачбифд**](iscardmanage-attachbyifd.md).

Чтобы повторно подключиться к смарт-карте, не вызывая **Detach** и [**аттачбихандле**](iscardmanage-attachbyhandle.md), вызовите [**Reconnect**](iscardmanage-reconnect.md).

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

[**аттачбифд**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**искардманаже**](iscardmanage.md)
</dt> <dt>

[**Повтор соединения**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
