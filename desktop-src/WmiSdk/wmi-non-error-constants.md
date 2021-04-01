---
description: Коды возврата WMI, указывающие состояние и не указывающие на ошибку.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Константы WMI, отличные от ошибок (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263924"
---
# <a name="wmi-non-error-constants"></a>Константы WMI, отличные от ошибок

Коды возврата WMI, указывающие состояние и не указывающие на ошибку.

Если операция не приводит к ошибке, WMI возвращает один из следующих кодов как **HRESULT** , указывающий состояние операции.

> [!Note]  
> Некоторые методы в классах WMI могут возвращать системные и сетевые коды ошибок (например, 64). Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки. Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно.

 

В C++ можно вызвать [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) и указать **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** в качестве модуля сообщения.

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ \_ без \_ ошибок**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Операция выполнена успешно.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ , \_ ложь**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Больше нет доступных объектов, число возвращаемых объектов меньше запрошенного числа или это конец перечисления. Это значение также возвращается при вызове этого метода со значением 0 для параметра *укаунт* .


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ \_ уже \_ существует**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



Предпринята попытка создать уже существующий объект или класс.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_Установка WBEM \_ \_ \_ по умолчанию**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Удалено переопределенное свойство. Это значение возвращается, чтобы сообщить, что исходное переопределенное значение было восстановлено в результате удаления.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**\_другой WBEM \_**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Элементы (объекты, классы и т. д.), которые сравниваются, не идентичны.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ , \_ TIMEDOUT**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Время ожидания вызова истекло. Это не условие ошибки. Поэтому могут также возвращаться некоторые результаты.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM, больше \_ \_ нет \_ \_ данных**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



В перечислении больше нет доступных данных, и пользователь должен завершить перечисление.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_Операция WBEM \_ S \_ отменена**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



Операция была намеренно или непреднамеренно отменена.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**\_ \_ Ожидание с WBEM**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Запрос все еще выполняется, и результаты еще не доступны.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_объекты с \_ ПОВТОРЯЮЩИМИСЯ \_ объектами WBEM**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



В результирующем наборе перечисления обнаружено несколько копий одного объекта.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_ \_ доступ к WBEM S \_ запрещен**
</dt> <dd> <dl> <dt>

262153 (0x40009)
</dt> <dt>



Пользователю отказано в доступе к некоторым, но не ко всем ресурсам.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_неполные \_ \_ результаты с WBEM**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



Пользователь не получил все запрошенные объекты из-за недоступных ресурсов (кроме нарушений безопасности).


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_ \_ ограниченная \_ Служба WBEM**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



Поставщик может иметь ограниченную службу.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**\_ \_ непрямое \_ Обновление WBEM**
</dt> <dd> <dl> <dt>

274434 (0x43002)
</dt> <dt>



Зарезервировано для последующего использования.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Header<br/>                   | <dl> <dt>Вбемкли. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Вбемкли. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды возврата WMI](wmi-return-codes.md)
</dt> </dl>

 

