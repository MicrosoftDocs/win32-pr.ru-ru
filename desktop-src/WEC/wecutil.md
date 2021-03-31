---
title: Wecutil.exe
description: Wecutil.exe — это служебная программа сборщика событий Windows, которая позволяет администратору создавать и администрировать подписки на события, пересылаемые из удаленных источников событий, поддерживающих протокол WS-Management.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353982"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe — это служебная программа сборщика событий Windows, которая позволяет администратору создавать и администрировать подписки на события, пересылаемые из удаленных источников событий, поддерживающих протокол WS-Management. Команды, параметры и значения параметров не учитывают регистр для этой служебной программы.

Если появится сообщение "сервер RPC недоступен" или "неизвестный интерфейс" при попытке запустить wecutil, необходимо запустить службу сборщика событий Windows (вексвк). Чтобы запустить вексвк, в командной строке с повышенными привилегиями введите **net start вексвк**.

## <a name="list-existing-subscriptions"></a>Список существующих подписок

Для перечисления существующих удаленных подписок на события используется следующий синтаксис.

``` syntax
wecutil { es | enum-subscription }
```

Если для получения имен подписок из выходных данных используется сценарий, необходимо обойти символы спецификации UTF-8 в первой строке выходных данных. В следующем сценарии показан пример того, как можно пропустить символы спецификации.

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a>Получение конфигурации подписки

Для просмотра данных конфигурации удаленной подписки на события используется следующий синтаксис.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Получить параметры конфигурации

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**
</dt> <dd>

Строка, однозначно определяющая подписку. Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: * значение***
</dt> <dd>

Значение типа, указывающее выходные данные конфигурации подписки. Может иметь *значение* "XML" или "сжатый", а по умолчанию — "сжатый". Если *значение параметра* — "XML", выходные данные выводятся в формате "XML". Если *значение параметра* — "сжатый", выходные данные выводятся в виде пар "имя-значение".

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *значение***
</dt> <dd>

Значение типа, указывающее, имеет ли выходные данные формат Юникода. *Значение* может быть "true" или "false". Если *значение* равно true, то выходные данные имеют формат Юникода, а если *значение* — false, то выходные данные не имеют формата Юникода.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Получение состояния среды выполнения подписки

Для вывода состояния среды выполнения подписки используется следующий синтаксис.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Получение параметров состояния

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**
</dt> <dd>

Строка, однозначно определяющая подписку. Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_Источник события**
</dt> <dd>

Значение, идентифицирующее компьютер, являющийся источником события для подписки на события. Это значение может быть полным доменным именем компьютера, NetBIOS-имени или адреса IP.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Настройка сведений о конфигурации подписки

Следующий синтаксис используется для задания данных конфигурации подписки путем изменения параметров подписки из командной строки или с помощью XML-файла конфигурации.

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a>Комментарии

Если в команде **wecutil SS** указано неправильное имя пользователя или пароль, ошибки не выводятся до тех пор, пока вы не просмотрите состояние выполнения подписки с помощью команды **wecutil GR** .

## <a name="set-configuration-parameters"></a>Установка параметров конфигурации

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**
</dt> <dd>

Строка, однозначно определяющая подписку. Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *конгиг \_ файл***
</dt> <dd>

Значение типа, указывающее путь к XML-файлу, содержащему сведения о конфигурации подписки. Путь может быть абсолютным или относительным для текущего каталога. Этот параметр можно использовать только с необязательными параметрами/кус и/КУП и является взаимоисключающим со всеми другими параметрами.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *значение***
</dt> <dd>

Значение, определяющее, следует ли включать или отключать подписку. Может иметь значение true или false. Значение по умолчанию — true, что включает подписку.

> [!Note]  
> При отключении подписки, инициированной сборщиком, источник событий переходит в неактивное состояние вместо отключения. В подписке, инициированной сборщиком, можно отключить источник событий независимо от подписки.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Описание***
</dt> <dd>

Значение типа, указывающее описание подписки на события.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ЕКС: *Дата и \_ время***
</dt> <dd>

Значение типа, указывающее срок действия подписки. *Дата \_ ВРЕМЯ* — это значение, заданное в стандартном формате XML или ISO8601: "гггг-мм-ddThh: мм: СС \[ . SSS \] \[ Z \] ", где "T" — это разделитель времени, а "Z" — время в формате UTC. Например, если *Дата и \_ время* имеют значение "2007-01-12T01:20:00", срок действия подписки составляет 12 января 2007 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/Ури: *URI***
</dt> <dd>

Значение типа, указывающее тип событий, потребляемых подпиской. Адрес исходного компьютера события вместе с универсальным кодом ресурса (URI) однозначно определяет источник событий. Строка URI используется для всех адресов источников событий в подписке.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/CM: *\_ режим конфигурации***
</dt> <dd>

Значение типа, указывающее режим конфигурации подписки на события. *Конфигурация \_ РЕЖИМ* может быть одной из следующих строк: "Обычная", "Custom", "минлатенци" или "MinBandwidth". Перечисление [**\_ \_ \_ режима конфигурации подписки EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) определяет режимы конфигурации. Параметры/дм,/ДМИ,/Хи и/дмлт можно указывать, только если для режима конфигурации задано значение Custom.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *запрос***
</dt> <dd>

Значение типа, указывающее строку запроса для подписки. Формат этой строки может отличаться для разных значений URI и применяться ко всем источникам событий в подписке.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/Диа: *диалект***
</dt> <dd>

Значение типа, указывающее диалект, используемый строкой запроса.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/КФ: *Формат***
</dt> <dd>

Значение типа, указывающее формат возвращаемых событий. *Формат* может быть "Events" или "рендередтекст". Если значение равно "Рендередтекст", то события возвращаются с помощью локализованных строк (например, строк описания событий), прикрепленных к событиям. По умолчанию используется значение *Format* "рендередтекст".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *языковой стандарт***
</dt> <dd>

Значение, указывающее языковой стандарт для доставки локализованных строк в формате отображаемого текста. *Языковой стандарт* — это идентификатор культуры языка или страны, например en-US. Этот параметр допустим только в том случае, если для параметра/КФ задано значение "Рендередтекст".

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ри: \[ *значение*\]**
</dt> <dd>

Значение, указывающее, какие события должны быть доставлены для подписки. Может иметь *значение* true или false. Если *значение* равно true, все существующие события считываются из источников событий подписки. Если *значение* равно false, доставляются только будущие (поступающие) события. Значение по умолчанию — true, если/ри указан без значения, а значение по умолчанию — false, если/ри не задан.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/ЛФ: *имя файла***
</dt> <dd>

Значение типа, указывающее локальный журнал событий, который используется для хранения событий, полученных из подписки на события.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/Пн: *Издатель***
</dt> <dd>

Значение типа, указывающее имя издателя события (поставщика). Он должен быть издателем, который владеет или импортирует журнал, заданный параметром/ЛФ.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/дм: *режим***
</dt> <dd>

Значение типа, указывающее режим доставки подписки. *Режим* может принимать значение push или Pull. Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/Дми: *число***
</dt> <dd>

Значение, указывающее максимальное количество элементов для пакетной доставки в подписке на события. Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/дмлт: *МС***
</dt> <dd>

Значение, указывающее максимальную задержку, разрешенную для доставки пакета событий. МС — это допустимое количество миллисекунд. Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Хи: *МС***
</dt> <dd>

Значение, указывающее интервал пульса для подписки. *МС* — это количество миллисекунд, использованных в интервале. Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *транспорта***
</dt> <dd>

Значение типа, указывающее имя транспорта, используемого для подключения к удаленному компьютеру источника событий.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ЕСА: *\_ Источник события***
</dt> <dd>

Значение типа, указывающее адрес исходного компьютера события. *Событие \_ Источник* — это строка, которая определяет компьютер источника событий с помощью полного доменного имени компьютера, NetBIOS-имени или IP адреса. Этот параметр можно использовать с параметрами/ЕСЕ,/АЕС,/RES или/Ун и/up.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ЕСЕ: *значение***
</dt> <dd>

Значение, определяющее, включать или отключать источник событий. Может иметь *значение* true или false. Значение по умолчанию — true, что включает источник события. Этот параметр используется только в том случае, если используется параметр/ЕСА.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/аес**
</dt> <dd>

Значение, добавляющее источник событий, заданный параметром/ЕСА, если источник события еще не является частью подписки на события. Если компьютер, указанный параметром/ЕСА, уже входит в подписку, отображается сообщение об ошибке. Этот параметр разрешен только в том случае, если используется параметр/ЕСА.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/RES**
</dt> <dd>

Значение, которое удаляет источник события, указанный параметром/ЕСА, если источник события уже является частью подписки на события. Если компьютер, указанный параметром/ЕСА, не входит в подписку, отображается сообщение об ошибке. Этот параметр разрешен только в том случае, если используется параметр/ЕСА.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/Ун: *имя пользователя***
</dt> <dd>

Значение, указывающее имя пользователя, используемое в учетных данных для подключения к источнику событий, указанному в параметре/ЕСА. Этот параметр разрешен только в том случае, если используется параметр/ЕСА.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/Up: *пароль***
</dt> <dd>

Значение типа, указывающее пароль для имени пользователя, указанного в параметре/ун. Учетные данные имени пользователя и пароля используются для подключения к источнику событий, указанному в параметре/ЕСА. Этот параметр разрешен только в том случае, если используется параметр/ун.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *транспортпорт***
</dt> <dd>

Значение, указывающее номер порта, используемый транспортом при соединении с удаленным компьютером источника событий.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/ХН: *имя***
</dt> <dd>

Значение типа, указывающее DNS-имя локального компьютера. Это имя используется удаленными источниками событий для отправки событий обратно и должно использоваться только для принудительных подписок.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/КТ: *тип***
</dt> <dd>

Значение типа, указывающее тип учетных данных, используемый для доступа к удаленным источникам событий. *Тип* может быть "default", "Negotiate", "Digest", "Basic" или "LocalMachine". Значение по умолчанию — "по умолчанию". Эти значения определены в перечислении [**\_ \_ \_ типа учетных данных подписки EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Кун: *имя пользователя***
</dt> <dd>

Значение, устанавливающее общие учетные данные пользователя, используемые для источников событий, не имеющих собственных учетных данных пользователя.

> [!Note]  
> Если этот параметр используется с параметром/c, то параметры имени пользователя и пароля для отдельных источников событий из файла конфигурации игнорируются. Если вы хотите использовать разные учетные данные для определенного источника событий, это значение можно переопределить, указав параметры/Ун и/up для определенного источника события в командной строке другой команды Set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/КУП: *пароль***
</dt> <dd>

Значение, которое задает пароль пользователя для учетных данных общего пользователя. Если для параметра *Password* задано значение \* (звездочка), то пароль считывается из консоли. Этот параметр допустим только в том случае, если указан параметр/кун.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ИКА: *отпечатки***
</dt> <dd>

Значение, задающее список отпечаток сертификата издателя, в списке с разделителями-запятыми.

> [!Note]  
> Этот параметр относится только к исходным подпискам, инициированным источником.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/АС: *разрешено***
</dt> <dd>

Значение, которое задает разделенный запятыми список строк, указывающий DNS-имена компьютеров, не являющихся доменами, которым разрешено инициировать подписки. Имена можно указать с помощью подстановочных знаков, например " \* . mydomain.com". По умолчанию этот список пустой.

> [!Note]  
> Этот параметр относится только к исходным подпискам, инициированным источником.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ДС: *запрещено***
</dt> <dd>

Значение, которое задает разделенный запятыми список строк, указывающий DNS-имена недоменных компьютеров, для которых запрещено инициировать подписки. Имена можно указать с помощью подстановочных знаков, например " \* . mydomain.com". По умолчанию этот список пустой.

> [!Note]  
> Этот параметр относится только к исходным подпискам, инициированным источником.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/АДК: *SDDL***
</dt> <dd>

Значение, которое задает строку в формате SDDL, указывающую, какие компьютеры домена разрешены или запрещены для инициирования подписок. Значение по умолчанию — разрешить всем компьютерам домена инициировать подписки.

> [!Note]  
> Этот параметр относится только к исходным подпискам, инициированным источником.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Создание новой подписки

Для создания подписки на события на удаленном компьютере используется следующий синтаксис.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Комментарии

Если в команде **wecutil CS** указано неправильное имя пользователя или пароль, ошибки не выводятся до тех пор, пока вы не просмотрите состояние выполнения подписки с помощью команды **wecutil GR** .

## <a name="creation-parameters"></a>Параметры создания

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**\_файл конфигурации**
</dt> <dd>

Значение типа, указывающее путь к XML-файлу, содержащему сведения о конфигурации подписки. Путь может быть абсолютным или относительным для текущего каталога.

Следующий код XML является примером файла конфигурации подписки, который создает подписку, инициированную сборщиком, для перенаправления событий из журнала событий приложений удаленного компьютера в журнал ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



Следующий код XML является примером файла конфигурации подписки, который создает созданную источником подписку для перенаправления событий из журнала событий приложений удаленного компьютера в журнал ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> При создании исходной инициированной подписки, если **алловедсаурцедомаинкомпутерс**, **алловедсаурценондомаинкомпутерс** / **иссуеркалист**, **алловедсубжектлист** и **DeniedSubjectList** все пусты, будет использоваться значение по умолчанию для **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; Общедоступный;;; NS) ". По умолчанию SDDL предоставляет членам группы домена "компьютеры домена", а также группы локальных сетевых служб (для локального сервера пересылки) возможность создавать события для этой подписки.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Кун: *имя пользователя***
</dt> <dd>

Значение, устанавливающее общие учетные данные пользователя, используемые для источников событий, не имеющих собственных учетных данных пользователя. Это значение применяется только к подпискам, инициированным сборщиком.

> [!Note]  
> Если этот параметр указан, то параметры имени пользователя и пароля для отдельных источников событий из файла конфигурации игнорируются. Если вы хотите использовать разные учетные данные для определенного источника событий, это значение можно переопределить, указав параметры/Ун и/up для определенного источника события в командной строке другой команды Set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/КУП: *пароль***
</dt> <dd>

Значение, которое задает пароль пользователя для учетных данных общего пользователя. Если для параметра *Password* задано значение " \* " (звездочка), то пароль считывается из консоли. Этот параметр допустим только в том случае, если указан параметр/кун.

</dd> </dl>

## <a name="delete-a-subscription"></a>Удаление подписки

Для удаления подписки на события используется следующий синтаксис.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Параметры удаления

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**
</dt> <dd>

Строка, однозначно определяющая подписку. Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки. Подписка, указанная в этом параметре, будет удалена.

</dd> </dl>

## <a name="retry-a-subscription"></a>Повтор подписки

Следующий синтаксис используется для повторного выполнения неактивной подписки путем попытки повторной активации всех или указанных источников событий путем установки соединения с каждым источником событий и отправки запроса на удаленную подписку в источник событий. Отключенные источники событий не повторяются.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Параметры повтора

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**
</dt> <dd>

Строка, однозначно определяющая подписку. Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки. Подписка, указанная в этом параметре, будет предпринята повторно.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_Источник события**
</dt> <dd>

Значение, идентифицирующее компьютер, являющийся источником события для подписки на события. Это значение может быть полным доменным именем компьютера, NetBIOS-имени или адреса IP.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Настройка службы сборщика событий Windows

Следующий синтаксис используется для настройки службы сборщика событий Windows для обеспечения возможности создания и поддержания подписок на события при перезагрузке компьютера. Сюда входит следующая процедура:

**Настройка службы сборщика событий Windows**

1.  Включите канал ForwardedEvents, если он отключен.
2.  Задержка запуска службы сборщика событий Windows.
3.  Запустите службу сборщика событий Windows, если она не запущена.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Настройка параметров сборщика событий

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *значение***
</dt> <dd>

Значение, определяющее, будет ли команда быстрой настройки запрашивать подтверждение. Может иметь значение true или false. Если значение — true, команда запросит подтверждение. Значением по умолчанию является false.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



 

 





