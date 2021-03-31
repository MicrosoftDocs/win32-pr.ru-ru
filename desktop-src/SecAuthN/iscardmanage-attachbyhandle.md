---
description: Создает канал связи со смарт-картой (ICC) с помощью маркера, возвращенного диспетчером ресурсов смарт-карты.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Метод Искардманаже:: Аттачбихандле'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910631"
---
# <a name="iscardmanageattachbyhandle-method"></a>Метод Искардманаже:: Аттачбихандле

\[Метод **аттачбихандле** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **аттачбихандле** создает канал связи со [*смарт-картой*](../secgloss/s-gly.md) (ICC) с помощью маркера, возвращенного [*диспетчером ресурсов*](../secgloss/r-gly.md)смарт-карты.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хикк* \[ окне\]
</dt> <dd>

Маркер смарт-карты.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений:



| Код возврата                                                                                   | Описание                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *хикк* .<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                     |



 

## <a name="remarks"></a>Комментарии

Чтобы присоединить [*средство чтения*](../secgloss/r-gly.md) Call [**аттачбифд**](iscardmanage-attachbyifd.md).

Освобождение вызова [**отсоединения**](iscardmanage-detach.md)вложений.

Чтобы повторно подключиться к смарт-карте, не вызывая [**Detach**](iscardmanage-detach.md) и **аттачбихандле**, вызовите [**Reconnect**](iscardmanage-reconnect.md).

Список всех методов, определенных интерфейсом [**искардманаже**](iscardmanage.md) , см. в разделе [**искардманаже**](iscardmanage.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения о кодах ошибок смарт-карт см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аттачбифд**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Соединил**](iscardmanage-detach.md)
</dt> <dt>

[**искардманаже**](iscardmanage.md)
</dt> <dt>

[**Повтор соединения**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
