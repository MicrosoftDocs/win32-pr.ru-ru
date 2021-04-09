---
title: Константы WINBIO_OPERATION_TYPE (Винбио \_ types. h)
description: Укажите тип выполняемой асинхронной операции.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137775"
---
# <a name="winbio_operation_type-constants"></a>\_ \_ Константы типа операции винбио

Следующие константы могут возвращаться биометрическая платформа Windows в [**\_ асинхронном \_ результате винбио**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) для указания типа выполняемой асинхронной операции.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_Операция винбио \_ None**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Операции не обнаружены.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_Операция винбио \_ открыта**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Был открыт сеанс биометрической метрики. Дополнительные сведения см. в разделе [**винбиоасинкопенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_закрытие операции \_ винбио**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Биометрическая сессия закрыта. Дополнительные сведения см. в разделе [**винбиоклосесессион**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**\_Проверка операции \_ винбио**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Образец биометрической метрики проверен на соответствие удостоверению пользователя. Дополнительные сведения см. в разделе [**винбиоверифи**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**ВИНБИО \_ операция \_ обнаружения**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Биометрическая выборка была захвачена и сравнена с существующим шаблоном. Дополнительные сведения см. в разделе [**винбиоидентифи**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**ВИНБИО \_ операция при \_ поиске \_ датчика**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Номер идентификатора биометрического блока был получен. Дополнительные сведения см. в разделе [**винбиолокатесенсор**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**\_ \_ Начало регистрации операции \_ винбио**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Инициирована биометрическая последовательность регистрации. Дополнительные сведения см. в разделе [**винбиоенроллбегин**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**\_ \_ запись регистрации винбио \_ операции**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Образец биометрической метрики был захвачен и добавлен в шаблон. Дополнительные сведения см. в разделе [**винбиоенроллкаптуре**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**\_ \_ фиксация регистрации операции винбио \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Завершено Завершение ожидающего шаблона биометрического метрики. Дополнительные сведения см. в разделе [**винбиоенроллкоммит**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**\_ \_ Отмена регистрации операции \_ винбио**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Незавершенный биометрический шаблон был отклонен. Дополнительные сведения см. в разделе [**винбиоенроллдискард**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_ \_ Регистрация перечислений операций винбио \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Подразделы для данного шаблона были перечислены. Дополнительные сведения см. в разделе [**винбиоенуменроллментс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**\_ \_ шаблон удаления винбио \_ операции**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Биометрическая шаблон удален из хранилища. Дополнительные сведения см. в разделе [**винбиоделететемплате**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_ \_ Пример записи операции \_ винбио**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Был собран образец биометрической метрики. Дополнительные сведения см. в разделе [**винбиокаптуресампле**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**ВИНБИО \_ операция \_ получения \_ Свойства**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Получено свойство сеанса биометрической метрики, единицы измерения или шаблона. Дополнительные сведения см. в разделе [**винбиожетпроперти**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_ \_ свойство набора операций \_ винбио**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Задано свойство "биометрическая сессия", "единица", "шаблон" или "учетная запись". Дополнительные сведения см. в разделе [**винбиосетпроперти**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ событие получения винбио \_ операции**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Не используется.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_ \_ блок блокировки операции \_ винбио**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Биометрическая единица заблокирована для монопольного использования в сеансе. Дополнительные сведения см. в разделе [**винбиолоккунит**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_ \_ единица разблокировки операции винбио \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Блокировка сеанса на биометрической единице была освобождена. Дополнительные сведения см. в разделе [**винбиаунлоккунит**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_ \_ единица управления ОПЕРАЦИей винбио \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Определенные поставщиком операции были выполнены над единицей управления. Дополнительные сведения см. в разделе [**винбиоконтролунит**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_ \_ \_ привилегированный доступ к единице управления Operation винбио \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Определенные привилегированные операции, определяемые поставщиком, выполнялись на единице управления. Дополнительные сведения см. в разделе [**винбиоконтролунитпривилежед**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**ВИНБИО \_ операция \_ Open \_ Framework**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Был открыт обработчик биометрической платформы.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**ВИНБИО \_ операция \_ закрытия \_ платформы**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Маркер биометрической платформы был закрыт. Дополнительные сведения см. в разделе [**винбиоклосефрамеворк**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_ \_ \_ поставщики служб ПЕРЕЧИСЛЕНИЯ для операций винбио \_**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Установленные поставщики биометрических служб были перечислены. Дополнительные сведения см. в разделе [**винбиоенумсервицепровидерс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ биометрические единицы ПЕРЕчислителя операции винбио \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Подключенные биометрические единицы были перечислены. Дополнительные сведения см. в разделе [**винбиоасинценумбиометрикунитс**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_ \_ базы данных перечислений операций винбио \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Зарегистрированные базы данных были перечислены. Дополнительные сведения см. в разделе [**винбиоенумдатабасес**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**\_ \_ Получение единиц операций \_ винбио**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Был создан биометрический модуль. Дополнительные сведения см. в разделе [**винбиоасинкмониторфрамеворкчанжес**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**\_ \_ Удаление единицы операции \_ винбио**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Биометрическая единица была удалена. Дополнительные сведения см. в разделе [**винбиоасинкмониторфрамеворкчанжес**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**ВИНБИО \_ операции \_ обнаружения \_ и \_ освобождения \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Зарезервировано. Это значение поддерживается начиная с Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**ВИНБИО \_ операции \_ проверки \_ и \_ освобождения \_ билета**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Зарезервировано. Это значение поддерживается начиная с Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_ \_ присутствие монитора винбио \_ Operation**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Механизм распознавания лиц или контроля IRI был включен. Дополнительные сведения см. в разделе [**винбиомониторпресенце**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Это значение поддерживается начиная с Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**ВИНБИО \_ операции \_ регистрации \_ SELECT**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Отдельный пользователь из группы лиц, представленных данными в буфере выборки, был указан для регистрации. Дополнительные сведения см. в разделе [**винбиоенроллселект**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect). Это значение поддерживается начиная с Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                                                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





