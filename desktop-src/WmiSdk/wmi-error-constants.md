---
description: При возникновении ошибки Инструментарий WMI возвращает код ошибки в виде значения HRESULT. Эти коды могут возвращаться сценариями, приложениями C++ или WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Константы ошибок WMI (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679fd0cb9714e2ee202b12195b10e72778564d7549ed4731d905603a11e073db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794314"
---
# <a name="wmi-error-constants"></a>Константы ошибок WMI

При возникновении ошибки Инструментарий WMI возвращает код ошибки в виде значения **HRESULT** . Эти коды могут возвращаться сценариями, приложениями C++ или [**WMIC**](wmic.md).

> [!Note]
>
> Следующая документация предназначена для разработчиков и ИТ-администраторов. Если вы являетесь пользователем, имеющим сообщение об ошибке, связанное с WMI, перейдите в [Служба поддержки Майкрософт](https://support.microsoft.com/) и найдите код ошибки, который вы видите в сообщении об ошибке. Дополнительные сведения об устранении неполадок со сценариями WMI и службой WMI см. в разделе [инструментарий WMI не работает](/previous-versions/tn-archive/ff406382(v=msdn.10)).
>
> Если инструментарий WMI возвращает сообщения об ошибках, имейте в виду, что они могут не указывать на проблемы в службе WMI или в поставщиках WMI. Сбои могут исходить из других частей операционной системы и возникать как ошибки через инструментарий WMI. При любых обстоятельствах не удаляйте репозиторий WMI как первое действие, поскольку удаление репозитория может привести к повреждению системы или установке приложений.
>
> чтобы получить дополнительные сведения об источнике проблемы, скачайте и запустите программу командной строки для диагностики [служебная программа для диагностики WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) . Это средство создает отчет, который обычно может изолировать источник проблемы и предоставить инструкции по ее устранению. Этот отчет также помогает в работе со службой поддержки Майкрософт. служебная программа для диагностики WMI можно скачать [здесь](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

Некоторые методы в классах WMI могут возвращать системные и сетевые коды ошибок (например, 64). Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки. Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно.

В следующем списке перечислены некоторые распространенные диапазоны ошибок.

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099
</dt> <dd>

Ошибки, возникающие в самом инструментарии WMI.

Не удалось выполнить определенную операцию WMI из-за

-   Ошибка в запросе, например запрос WQL, или учетная запись не имеет нужных разрешений.
-   Проблема с инфраструктурой WMI, например неправильная регистрация CIM или DCOM.

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

Ошибки, происходящие в основной операционной системе. Инструментарий WMI может вернуть ошибку такого типа из-за внешней ошибки, например ошибки безопасности DCOM.

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

Ошибки, происходящие в DCOM. Например, конфигурация DCOM для операций на удаленном компьютере может быть неверной.

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

Ошибка, полученная из ADSI (интерфейсов служб Active Directory) или LDAP (протокол Lightweight Directory Access), например, сбой доступа Active Directory при использовании поставщиков Active Directory WMI.

</dd> </dl>

Некоторые методы в классах WMI могут возвращать системные и сетевые коды ошибок (например, 64). Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки. Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно. в C++ можно вызвать [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) и указать **C: \\ Windows \\ System32 \\ wbem \\wmiutils.dll** в качестве модуля сообщения.

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**\_сбой WBEM E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Сбой вызова.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ не \_ найден**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Не удается найти объект.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**\_ \_ отказано в доступе к WBEM \_**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003)
</dt> <dt>



У текущего пользователя нет разрешения на выполнение действия.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_ \_ сбой поставщика WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Произошел сбой поставщика в некоторый момент, кроме инициализации.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_несоответствие типов электронной почты WBEM \_ \_**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Обнаружено несоответствие типов.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ \_ \_ , нехваткой \_ памяти**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Недостаточно памяти для операции.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_ \_ Недопустимый контекст для WBEM E \_**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007)
</dt> <dt>



Недопустимый объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_ \_ Недопустимый параметр "WBEM E" \_**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Один из параметров вызова указан неправильно.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ \_ недоступен**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



Ресурс, обычно удаленный сервер, в настоящее время недоступен.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**\_ \_ критическая ошибка WBEM E \_**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100A)
</dt> <dt>



Произошла внутренняя, критическая и непредвиденная ошибка. Сообщите об ошибке службе технической поддержки Майкрософт.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_ \_ Недопустимый \_ поток WBEM E**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100B)
</dt> <dt>



В течение удаленного сеанса поврежден один или несколько сетевых пакетов.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



Функция или операция не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**\_ \_ Недопустимый \_ суперкласс для WBEM**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100D)
</dt> <dt>



Указан недопустимый родительский класс.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ недопустимое \_ пространство имен**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



Не удается найти указанное пространство имен.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_ \_ Недопустимый \_ объект для WBEM**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



Указан недопустимый экземпляр.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_ \_ Недопустимый \_ класс WBEM E**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010)
</dt> <dt>



Указан недопустимый класс.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_поставщик WBEM \_ E \_ не \_ найден**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011)
</dt> <dt>



Поставщик, указанный в схеме, не имеет соответствующей регистрации.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_ \_ недействительная \_ Регистрация поставщика WBEM E \_**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



Поставщик, указанный в схеме, имеет неправильную или неполную регистрацию.

Эта ошибка может быть вызвана множеством условий, включая следующие.

-   Пропущенная команда [ \# пространства имен pragma](pragma-namespace.md) в файле MOF-файл (MOF), используемом для регистрации поставщика. Поставщик может быть зарегистрирован в неправильном пространстве имен WMI.
-   Не удалось получить регистрацию COM.
-   Недопустимая модель размещения. Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).
-   В регистрации указан недопустимый класс.
-   Сбой создания экземпляра или наследования от класса [**\_ \_ Win32Provider**](--win32provider.md) для создания регистрации поставщика в MOF-файле.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_ \_ \_ сбой загрузки поставщика WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013)
</dt> <dt>



COM не может найти поставщика, на которого ссылается схема.

Эта ошибка может быть вызвана множеством условий, включая следующие.

-   Поставщик использует библиотеку DLL WMI, которая не соответствует lib-файлу, используемому при построении поставщика.
-   Библиотека DLL поставщика или любая из библиотек DLL, от которых он зависит, повреждена.
-   Поставщику не удалось экспортировать [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).
-   Внутрипроцессный поставщик не был зарегистрирован с помощью команды **regsvr32** .
-   Внутрипроцессный поставщик не был зарегистрирован с помощью параметра **/regserver** . Например, **myprog.exe/RegServer**.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ Ошибка инициализации WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Не удалось инициализировать компонент, например поставщик, по внутренним причинам.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_ \_ сбой транспорта с WBEM E \_**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015)
</dt> <dt>



Ошибка сети, которая не допустила нормальных операций.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ недействительная \_ Операция WBEM E**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



Запрошенная операция недопустима. Эта ошибка обычно является ответом на недопустимые попытки удалить классы или свойства.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ \_ Недопустимый запрос для WBEM E \_**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



Синтаксически недопустимый запрос.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_ \_ Недопустимый \_ тип запроса WBEM E \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Запрошенный язык запросов не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ уже \_ существует**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



В операции размещения был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**Переопределение для WBEM \_ E \_ \_ не \_ разрешено**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101A)
</dt> <dt>



Невозможно выполнить операцию добавления для этого квалификатора, так как объект-владелец не допускает переопределения.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_ \_ распространяемый квалификатор WBEM \_**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101B)
</dt> <dt>



Пользователь попытался удалить квалификатор, который не является владельцем. Квалификатор был унаследован от класса-родителя.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_ \_ распространяемое свойство WBEM \_**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101C)
</dt> <dt>



Пользователь попытался удалить свойство, владельцем которого он не является. Свойство было унаследовано от класса-родителя.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**\_ \_ непредвиденное непредусмотренное в WBEM**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101D)
</dt> <dt>



Клиент сделал непредвиденную и недопустимую последовательность вызовов, например вызов [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) перед вызовом [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**\_ \_ Недопустимая операция в WBEM E \_**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101E)
</dt> <dt>



Пользователь запросил недопустимую операцию, например, порождение класса из экземпляра.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ не может \_ быть \_ ключом**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101F)
</dt> <dt>



Недопустимая попытка указать квалификатор ключа для свойства, которое не может быть ключом. Ключи указываются в определении класса объекта и не могут быть изменены для каждого отдельного экземпляра.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_неполный \_ \_ класс WBEM E**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020)
</dt> <dt>



Текущий объект не является допустимым определением класса. Либо он неполон, либо не зарегистрирован в WMI с помощью [**SWbemObject. постановки \_**](swbemobject-put-.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ \_ Недопустимый \_ синтаксис WBEM E**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



Синтаксически недопустимый запрос.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**\_ \_ недекорированный объект WBEM E \_**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022)
</dt> <dt>



Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**\_только для \_ чтения с WBEM \_**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Была предпринята попытка изменить свойство, доступное только для чтения.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_поставщик WBEM \_ E \_ не \_ поддерживает**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Поставщик не может выполнить запрошенную операцию. Это может включать слишком сложный запрос, получение экземпляра, создание или обновление класса, удаление класса или перечисление класса.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**\_класс WBEM \_ E \_ имеет \_ дочерние элементы**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025)
</dt> <dt>



Предпринята попытка внести изменение, которое сделает подкласс недействительным.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**\_ \_ у класса WBEM E \_ есть \_ экземпляры**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026)
</dt> <dt>



Предпринята попытка удалить или изменить класс, имеющий экземпляры.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_запрос WBEM \_ E \_ не \_ реализован**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027)
</dt> <dt>



Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**\_ \_ недопустимое \_ значение NULL для WBEM E**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Значение Nothing или **null** было указано для свойства, которое должно иметь значение, например, помеченное квалификатором [**Key**](key-qualifier.md), [**индексированным**](optional-qualifiers.md)или **Not \_ null** .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM \_ E \_ Недопустимый \_ Тип квалификатора \_**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029)
</dt> <dt>



Указано значение типа Variant для квалификатора, которое не является допустимым типом квалификатора.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_ \_ Недопустимый \_ тип свойства WBEM \_**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102A)
</dt> <dt>



Для свойства указан недопустимый тип CIM.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_значение WBEM E \_ выходит за пределы допустимого \_ \_ \_ диапазона**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



Запрос был выполнен с использованием значения вне допустимого диапазона или несовместим с типом.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ не может \_ быть \_ SINGLETON**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102C)
</dt> <dt>



Предпринята недопустимая попытка создать Singleton класса, например, когда класс является производным от класса, не являющегося Singleton-классом.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ Недопустимый \_ \_ тип CIM**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102D)
</dt> <dt>



Указан недопустимый тип CIM.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ \_ Недопустимый \_ метод WBEM E**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



Запрошенный метод недоступен.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ недопустимые \_ \_ Параметры метода**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Для метода указаны недопустимые параметры.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_ \_ системное свойство WBEM E \_**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030)
</dt> <dt>



Предпринята попытка получить квалификаторы для системного свойства.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_ \_ неправильное \_ свойство WBEM E**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031)
</dt> <dt>



Тип свойства не распознан.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**\_вызов WBEM \_ E \_ отменен**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032)
</dt> <dt>



Асинхронный процесс был отменен внутренним образом или пользователем. Обратите внимание, что из-за времени и природы асинхронной операции операция может быть недействительно отменена.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ , \_ Завершение работы \_**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033)
</dt> <dt>



Пользователь запросил операцию, пока WMI находится в процессе завершения работы.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ распространенный метод WBEM \_**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034)
</dt> <dt>



Предпринята попытка повторно использовать существующее имя метода из родительского класса, и подписи не совпадают.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_ \_ неподдерживаемый параметр в WBEM E \_**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035)
</dt> <dt>



Одно или несколько значений параметров, например, текст запроса, являются слишком сложными или не поддерживаются. Поэтому WMI запрашивает повтор операции с более простыми параметрами.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ . \_ отсутствует \_ \_ идентификатор параметра**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036)
</dt> <dt>



В вызове метода отсутствовал параметр.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ \_ Недопустимый \_ идентификатор параметра WBEM E \_**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037)
</dt> <dt>



Недопустимый квалификатор [**идентификатора**](standard-wmi-qualifiers.md) параметра метода.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ \_ непоследовательные \_ \_ идентификаторы параметров в WBEM E**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038)
</dt> <dt>



Один или несколько параметров метода имеют непоследовательные квалификаторы [**ID**](standard-wmi-qualifiers.md) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ идентификатор параметра WBEM \_ E \_ в \_ RETVAL**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039)
</dt> <dt>



Возвращаемое значение метода имеет квалификатор [**идентификатора**](standard-wmi-qualifiers.md) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ Недопустимый \_ \_ путь к объекту**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



Указан недопустимый путь к объекту.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM. не \_ \_ хватает \_ \_ места на диске \_**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103B)
</dt> <dt>



На диске недостаточно места или достигнут предел в 4 ГБ для репозитория WMI (репозиторий CIM).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**\_буфер E \_ WBEM \_ слишком \_ мал**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103C)
</dt> <dt>



Указанный буфер слишком мал для размещения всех объектов в перечислителе или для чтения строкового свойства.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_ \_ неподдерживаемое \_ расширение размещения WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103D)
</dt> <dt>



Поставщик не поддерживает запрошенную операцию размещения.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_неизвестный \_ \_ тип объекта \_ WBEM**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103E)
</dt> <dt>



При упаковке обнаружен объект с неверным типом или версией.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_неизвестный \_ \_ тип пакетов \_ WBEM**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103F)
</dt> <dt>



При упаковке обнаружен пакет с неверным типом или версией.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**\_несоответствие \_ версии модуля WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040)
</dt> <dt>



Пакет имеет неподдерживаемую версию.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**\_ \_ \_ недействительная \_ подпись WBEM E**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041)
</dt> <dt>



Вероятно, пакет поврежден.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_ \_ Недопустимый \_ квалификатор WBEM E**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042)
</dt> <dt>



Предпринята попытка несовпадения квалификаторов, например помещение \[ ключа \] в объект, а не свойства.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ Недопустимый \_ дублирующийся параметр WBEM E \_**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043)
</dt> <dt>



В методе CIM объявлен дублирующийся параметр.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**\_ \_ слишком \_ большой объем \_ данных в WBEM**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044)
</dt> <dt>



Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**\_сервер WBEM \_ E \_ \_ занят**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045)
</dt> <dt>



Не удалось вызвать [**ивбемобжектсинк:: обозначение**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) . Поставщик может перезапустить событие.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**\_ \_ Недопустимый \_ флаг WBEM E**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046)
</dt> <dt>



Указана недопустимая разновидность квалификатора.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ циклическая \_ ссылка на WBEM E**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047)
</dt> <dt>



Предпринята попытка создать циклическую ссылку (например, производный от себя класс).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**\_ \_ неподдерживаемое \_ обновление класса WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048)
</dt> <dt>



Указанный класс не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ е \_ не \_ может \_ изменить \_ наследование ключа**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049)
</dt> <dt>



Предпринята попытка изменить ключ, когда в экземплярах или подклассах уже используется ключ.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ не \_ может \_ изменить \_ наследование индекса**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050)
</dt> <dt>



Предпринята попытка изменить индекс, если в экземплярах или подклассах уже используется индекс.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**\_ \_ слишком \_ много \_ свойств WBEM**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051)
</dt> <dt>



Предпринята попытка создать больше свойств, чем поддерживается текущей версией класса.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**\_несоответствие \_ \_ типа обновления \_ WBEM**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052)
</dt> <dt>



Свойство было переопределено с конфликтующим типом в производном классе.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**\_Переопределение \_ обновления WBEM E \_ \_ не \_ разрешено**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053)
</dt> <dt>



Попытка была выполнена в производном классе для переопределения квалификатора, который не может быть переопределен.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_ \_ \_ распространяемый метод WBEM E Update \_**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054)
</dt> <dt>



Метод был повторно объявлен с конфликтующей сигнатурой в производном классе.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_метод WBEM \_ E \_ не \_ реализован**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055)
</dt> <dt>



Предпринята попытка выполнить метод, не помеченный как \[ реализованный \] в каком-либо соответствующем классе.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_метод WBEM \_ E \_ отключен**
</dt> <dd> <dl> <dt>


</dt> <dt>



Предпринята попытка выполнить метод, помеченный как \[ отключенный \] .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**Подсистема \_ \_ обновления WBEM \_ занята**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057)
</dt> <dt>



Обновитель занят другой операцией.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_ \_ неанализируемый запрос WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058)
</dt> <dt>



Синтаксически недопустимый запрос фильтрации.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**\_ \_ \_ класс событий WBEM E \_ Not**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059)
</dt> <dt>



Предложение FROM запроса фильтрации ссылается на класс, который не является классом событий (производным от [**\_ \_ события**](--event.md)).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ . \_ отсутствует \_ Группа \_ в**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105A)
</dt> <dt>



Предложение GROUP BY использовано без соответствующего предложения GROUP WITHIN.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**\_ \_ отсутствует \_ список агрегирования для WBEM E \_**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105B)
</dt> <dt>



Использовано предложение GROUP BY. Статистическая обработка всех свойств не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**\_свойство WBEM \_ E \_ не \_ является \_ объектом**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105C)
</dt> <dt>



Точечная нотация использована для свойства, которое не является внедренным объектом.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**\_ \_ вычисление на WBEM E \_ по \_ объектам**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105D)
</dt> <dt>



Предложение GROUP BY ссылается на свойство, которое является внедренным объектом, без использования точечной нотации.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_ \_ неинтерпретируемый \_ запрос поставщика WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105F)
</dt> <dt>



В запросе на регистрацию поставщика событий ([**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md)) не указаны классы, для которых были предоставлены события.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**\_средство WBEM E \_ BACKUP \_ RESTORE \_ \_ работает WinMgmt**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060)
</dt> <dt>



Был сделан запрос на резервное копирование или восстановление репозитория во время его использования WinMgmt.exe или процессом SVCHOST, который содержит службу WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**\_ \_ переполнение очереди WBEM E \_**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061)
</dt> <dt>



Очередь асинхронной доставки переполнена из-за слишком высокой скорости работы потребителя событий.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**\_ \_ отсутствуют права доступа \_ WBEM \_**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062)
</dt> <dt>



Не удалось выполнить операцию, так как клиент не имеет необходимых прав безопасности.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_ \_ Недопустимый \_ оператор WBEM E**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063)
</dt> <dt>



Недопустимый оператор для этого типа свойства.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ локальные \_ учетные данные WBEM E**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064)
</dt> <dt>



Пользователь указал имя пользователя, пароль или центр в локальном соединении. Пользователь должен использовать пустое имя пользователя и пароль и зависеть от безопасности по умолчанию.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ не может \_ быть \_ абстрактным**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065)
</dt> <dt>



Класс был создан абстрактным, если его родительский класс не является абстрактным.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**\_ \_ доизмененный объект WBEM E \_**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066)
</dt> <dt>



Измененный объект записан без **флага WBEM. указан флаг \_ \_ \_ уточненных \_ квалификаторов** .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_клиент WBEM \_ с \_ слишком \_ высокой скоростью**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067)
</dt> <dt>



Клиент не получал объекты достаточно быстро из перечисления. Эта константа возвращается, когда клиент создает объект перечисления, но не извлекает объекты из перечислителя в течение отведенного времени, что приводит к резервному копированию кэша объектов перечислителя.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**\_ \_ нулевой \_ дескриптор безопасности \_ WBEM**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068)
</dt> <dt>



Использован дескриптор безопасности со значением NULL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**\_ \_ время \_ ожидания WBEM истекло**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069)
</dt> <dt>



Время ожидания операции истекло.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**\_ \_ недействительная \_ Ассоциация WBEM E**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



Недопустимая связь.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**\_ \_ неоднозначная \_ операция в WBEM**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106B)
</dt> <dt>



Операция была неоднозначным.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_ \_ нарушение квоты WBEM E \_**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106C)
</dt> <dt>



Инструментарий WMI занимает слишком много памяти. Это может быть вызвано недостатком доступности памяти или чрезмерным потреблением памяти системой WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_ \_ конфликт транзакции WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106D)
</dt> <dt>



Операция привела к конфликту транзакций.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_ \_ принудительный \_ откат от WBEM**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106E)
</dt> <dt>



Транзакция вынуждена выполнить откат.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**\_ \_ неподдерживаемый \_ языковой стандарт WBEM E**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106F)
</dt> <dt>



Языковой стандарт, используемый в вызове, не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**неактуальный \_ \_ маркер WBEM \_ \_ \_**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070)
</dt> <dt>



Неактуальный объектный обработчик.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**\_ \_ не удалось подключиться к WBEM \_**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071)
</dt> <dt>



не удалось подключиться к базе данных SQL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_ \_ Недопустимый \_ запрос маркера WBEM E \_**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072)
</dt> <dt>



Запрос на обработку недопустим.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_ \_ \_ \_ слишком длинное имя свойства \_ WBEM E**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073)
</dt> <dt>



Имя свойства содержит более 255 символов.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**\_ \_ имя класса WBEM \_ E \_ слишком \_ длинное**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074)
</dt> <dt>



Имя класса содержит более 255 символов.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**\_ \_ \_ \_ слишком длинное имя метода \_ WBEM E**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075)
</dt> <dt>



Имя метода содержит более 255 символов.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**\_ \_ \_ \_ слишком длинное имя квалификатора \_ WBEM E**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076)
</dt> <dt>



Имя квалификатора содержит более 255 символов.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**\_команда WBEM E \_ повторного выполнения \_**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077)
</dt> <dt>



необходимо повторно запустить команду SQL, так как существует взаимоблокировка SQL. он может быть возвращен только в том случае, если данные хранятся в базе данных SQL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**несоответствие версии WBEM \_ E \_ Database \_ ver \_**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078)
</dt> <dt>



Версия базы данных не соответствует версии, которая обрабатывается драйвером репозитория.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**\_ \_ Удаление запрета на WBEM \_**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079)
</dt> <dt>



Инструментарию WMI не удается выполнить операцию удаления, так как он не разрешен поставщиком.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**\_ \_ расстановка ЗАПРЕТов WBEM \_**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107A)
</dt> <dt>



Инструментарию WMI не удается выполнить операцию размещения, поскольку он не разрешен поставщиком.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ Недопустимый \_ языковой стандарт WBEM E**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080)
</dt> <dt>



Указанный идентификатор локали недопустим для операции.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_поставщик WBEM \_ E \_ приостановлен**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081)
</dt> <dt>



Поставщик приостановлен.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_ \_ требуется синхронизация WBEM \_ E**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082)
</dt> <dt>



Объект должен быть записан в репозиторий WMI и повторно извлечен до того, как запрошенная операция может быть выполнена. Эта константа возвращается, когда объект должен быть зафиксирован и получен для просмотра значения свойства.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ \_ No \_ схема**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083)
</dt> <dt>



Не удается завершить операцию; нет доступных схем.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_поставщик WBEM \_ E \_ уже \_ зарегистрирован**
</dt> <dd> <dl> <dt>

02147750020 (0x119FD010)
</dt> <dt>



Поставщик не может быть зарегистрирован, так как он уже зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_поставщик WBEM \_ E \_ не \_ зарегистрирован**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085)
</dt> <dt>



Поставщик не зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_ \_ Неустранимая \_ ошибка транспорта WBEM \_**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086)
</dt> <dt>



Произошла неустранимая ошибка транспорта.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_ \_ требуется зашифрованное \_ Подключение WBEM E \_**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087)
</dt> <dt>



Пользователь попытался задать имя компьютера или домена без зашифрованного соединения.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**\_ \_ \_ истекло время ожидания поставщика WBEM E \_**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088)
</dt> <dt>



Поставщику не удалось сообщить о результатах в течение указанного времени ожидания.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ , \_ без \_ ключа**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089)
</dt> <dt>



Пользователь попытался разместить экземпляр без определенного ключа.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_поставщик WBEM \_ E \_ отключен**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108A)
</dt> <dt>



Пользователь попытался зарегистрировать экземпляр поставщика, но COM-сервер для экземпляра поставщика был выгружен.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**\_ \_ \_ слишком \_ широкая вбемессная регистрация**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001)
</dt> <dt>



Регистрация поставщика перекрывается с доменом системных событий.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**\_ \_ \_ слишком \_ точная регистрация вбемесс E**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002)
</dt> <dt>



Предложение WITHIN в этом запросе не использовалось.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**ВБЕМЕСС \_ E \_ \_ не является \_ привилегированным**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003)
</dt> <dt>



У этого компьютера нет необходимых разрешений на доступ к домену для поддержки функций безопасности, связанных с созданным экземпляром подписки. обратитесь к администратору домена, чтобы добавить этот компьютер в группу доступа Windows авторизации.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ , \_ Повторная попытка \_ позже**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001)
</dt> <dt>



Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**\_ \_ состязание за ресурсы WBEM \_**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002)
</dt> <dt>



Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ имя квалификатора \_**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001)
</dt> <dt>



Требуется имя квалификатора.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**\_ \_ Ожидаемый вбеммоф \_ E**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002)
</dt> <dt>



Ожидается точка с запятой или "=".


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**ВБЕММОФ \_ E \_ ожидаемая \_ открывающая \_ фигурная скобка**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003)
</dt> <dt>



Ожидалась открывающая фигурная скобка.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**ВБЕММОФ \_ E \_ ожидалась \_ закрывающая \_ фигурная скобка**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004)
</dt> <dt>



Отсутствует закрывающая фигурная скобка или недопустимый элемент массива.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**ВБЕММОФ \_ E \_ ожидаемая \_ закрывающая \_ скобка**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005)
</dt> <dt>



Ожидается закрывающая скобка.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**ВБЕММОФ \_ E \_ ожидаемая \_ закрывающая \_ скобка**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006)
</dt> <dt>



Требуется закрывающая круглая скобка.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**ВБЕММОФ \_ E \_ недопустимое \_ постоянное \_ значение**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007)
</dt> <dt>



Числовое значение за пределами диапазона или строк без кавычек.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**\_ \_ Ожидаемый \_ идентификатор типа вбеммоф E \_**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008)
</dt> <dt>



Требуется идентификатор типа.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**\_ \_ ожидаемая \_ открытая \_ скобка вбеммоф E**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009)
</dt> <dt>



Ожидается открывающая скобка.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**ВБЕММОФ \_ E \_ нераспознанный \_ токен**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400A)
</dt> <dt>



Непредвиденный токен в файле.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**ВБЕММОФ \_ E \_ нераспознанный \_ тип**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Нераспознанный или неподдерживаемый идентификатор типа.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ \_ имя свойства**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Требуется имя свойства или метода.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**ВБЕММОФ \_ E \_ TYPEDEF \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400D)
</dt> <dt>



Определения типов и перечислимые типы не поддерживаются.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**\_ \_ непредвиденный псевдоним вбеммоф E \_**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400E)
</dt> <dt>



Только ссылка на объект класса может иметь значение псевдонима.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**ВБЕММОФ \_ E \_ непредвиденная \_ \_ Инициализация массива**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400F)
</dt> <dt>



Непредвиденная инициализация массива. Массивы должны быть объявлены с помощью \[ \] .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ \_ синтаксис прав**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010)
</dt> <dt>



Недопустимый синтаксис пути к пространству имен.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ дубликат \_**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011)
</dt> <dt>



Дублирующиеся описатели прав.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**ВБЕММОФ \_ E \_ Недопустимая \_ директива pragma**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012)
</dt> <dt>



После [ \# директивы pragma](pragma-namespace.md) должно следовать допустимое ключевое слово.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ синтаксис пространства имен \_**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013)
</dt> <dt>



Недопустимый синтаксис пути к пространству имен.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ \_ имя класса**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014)
</dt> <dt>



Непредвиденный символ в имени класса должен быть идентификатором.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**\_несоответствие \_ типов вбеммоф E \_**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015)
</dt> <dt>



Указанное значение не может быть выполнено в соответствующий тип.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ имя псевдонима \_**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016)
</dt> <dt>



За знаком доллара должно следовать имя псевдонима в качестве идентификатора.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**ВБЕММОФ \_ E \_ недопустимое \_ \_ объявление класса**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017)
</dt> <dt>



Недопустимое объявление класса.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**ВБЕММОФ \_ E \_ недопустимое \_ \_ объявление экземпляра**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018)
</dt> <dt>



Недопустимое объявление экземпляра. Оно должно начинаться с "экземпляр"


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**\_ \_ Ожидаемый доллар вбеммоф E \_**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019)
</dt> <dt>



Ожидаемый знак доллара. Псевдоним в формате "$name" должен следовать за ключевым словом "AS".


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_КВАЛИФИКАТОР вбеммоф E \_ Цимтипе \_**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401A)
</dt> <dt>



Квалификатор "ЦИМТИПЕ" не может быть указан непосредственно в MOF-файле. Используйте нотацию стандартного типа.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**ВБЕММОФ \_ E, \_ повторяющееся \_ свойство**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401B)
</dt> <dt>



В MOF обнаружено повторяющееся имя свойства.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**ВБЕММОФ \_ E \_ Недопустимая \_ Спецификация пространства имен \_**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401C)
</dt> <dt>



Недопустимый синтаксис пространства имен. Ссылки на другие серверы не допускаются.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**ВБЕММОФ \_ \_ за пределами \_ \_ диапазона**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401D)
</dt> <dt>



Значение вне допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ файл**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401E)
</dt> <dt>



Файл не является допустимым текстовым MOF-файлом или двоичным MOF-файлом.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**\_ \_ встроенные псевдонимы вбеммоф E \_ \_**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401F)
</dt> <dt>



Внедренные объекты не могут быть псевдонимами.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**ВБЕММОФ \_ \_ массив значений NULL E \_ \_ ELEM**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020)
</dt> <dt>



Элементы NULL в массиве не поддерживаются.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**ВБЕММОФный \_ \_ квалификатор дубликата \_**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021)
</dt> <dt>



Квалификатор использовался более одного раза для объекта.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**\_ \_ Ожидаемый \_ Тип флага вбеммоф E \_**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022)
</dt> <dt>



Ожидался тип разновидности, например **тоинстанце**, **ToSubClass**, **енаблеоверриде** или **DisableOverride**.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**\_ \_ несовместимые \_ типы разновидностей вбеммоф E \_**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023)
</dt> <dt>



Объединение **енаблеоверриде** и **DisableOverride** с одним и тем же квалификатором не допускается.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**ВБЕММОФ \_ E \_ несколько \_ псевдонимов**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024)
</dt> <dt>



Псевдоним нельзя использовать дважды.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**ВБЕММОФ \_ E \_ несовместимая \_ разновидность \_ TYPES2**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025)
</dt> <dt>



Сочетание **ограничений Restricted**, **тоинстанце** и **ToSubClass** не допускается.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**ВБЕММОФ \_ е \_ нет \_ \_ возвращенных массивов**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026)
</dt> <dt>



Методы не могут возвращать значения массива.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**ВБЕММОФ \_ E \_ должен \_ быть \_ in \_ или \_ out**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027)
</dt> <dt>



Аргументы должны иметь квалификатор **in** или **out** .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**\_ \_ Недопустимый \_ синтаксис флагов вбеммоф E \_**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028)
</dt> <dt>



Недопустимый синтаксис flags.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**ВБЕММОФ \_ E \_ , ожидаемая \_ скобка \_ или \_ неверный \_ тип**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029)
</dt> <dt>



Отсутствует последняя фигурная скобка и точка с запятой для класса.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**ВБЕММОФ \_ E \_ неподдерживаемое \_ \_ значение CIMV22 куал \_**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402A)
</dt> <dt>



Функция CIM версии 2,2 не поддерживается для значения квалификатора.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**ВБЕММОФ \_ E \_ неподдерживаемый \_ \_ тип данных \_ CIMV22**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402B)
</dt> <dt>



Тип данных CIM версии 2,2 не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ \_ синтаксис DELETEINSTANCE**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402C)
</dt> <dt>



Недопустимый синтаксис удаления экземпляра. Оно должно быть `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ синтаксис квалификатора \_**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402D)
</dt> <dt>



Недопустимый синтаксис квалификатора. Оно должно иметь значение `qualifiername:type=value,scope(class|instance), flavorname`.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_КВАЛИФИКАТОР вбеммоф E \_ \_ используется \_ вне \_ области видимости**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402E)
</dt> <dt>



Квалификатор используется за пределами области действия.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**ВБЕММОФ \_ E \_ Ошибка \_ создания \_ временного \_ файла**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402F)
</dt> <dt>



Ошибка при создании временного файла. Временный файл является промежуточным этапом в компиляции MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**\_Ошибка вбеммоф \_ E \_ : недопустимый \_ включаемый \_ файл**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030)
</dt> <dt>



Файл, включенный в MOF командой препроцессора [ \# , является](-include.md) недопустимым.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ \_ синтаксис делетекласс**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031)
</dt> <dt>



Недопустимый синтаксис команд препроцессора: [ \# pragma DeleteInstance](pragma-deleteinstance.md) или [ \# pragma делетекласс](pragma-deleteclass.md) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Заголовок<br/>                   | <dl> <dt>Вбемкли. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Вбемкли. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды возврата WMI](wmi-return-codes.md)
</dt> </dl>

 

