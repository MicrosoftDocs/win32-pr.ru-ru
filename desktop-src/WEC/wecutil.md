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
# <a name="wecutilexe"></a><span data-ttu-id="3e168-104">Wecutil.exe</span><span class="sxs-lookup"><span data-stu-id="3e168-104">Wecutil.exe</span></span>

<span data-ttu-id="3e168-105">Wecutil.exe — это служебная программа сборщика событий Windows, которая позволяет администратору создавать и администрировать подписки на события, пересылаемые из удаленных источников событий, поддерживающих протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="3e168-105">Wecutil.exe is a Windows Event Collector utility that enables an administrator to create and manage subscriptions to events forwarded from remote event sources that support the WS-Management protocol.</span></span> <span data-ttu-id="3e168-106">Команды, параметры и значения параметров не учитывают регистр для этой служебной программы.</span><span class="sxs-lookup"><span data-stu-id="3e168-106">Commands, options, and option values are case-insensitive for this utility.</span></span>

<span data-ttu-id="3e168-107">Если появится сообщение "сервер RPC недоступен" или "неизвестный интерфейс" при попытке запустить wecutil, необходимо запустить службу сборщика событий Windows (вексвк).</span><span class="sxs-lookup"><span data-stu-id="3e168-107">If you receive a message that says "The RPC server is unavailable" or "The interface is unknown" when you try to run wecutil, then you need to start the Windows Event Collector service (wecsvc).</span></span> <span data-ttu-id="3e168-108">Чтобы запустить вексвк, в командной строке с повышенными привилегиями введите **net start вексвк**.</span><span class="sxs-lookup"><span data-stu-id="3e168-108">To start wecsvc, at an elevated command prompt type **net start wecsvc**.</span></span>

## <a name="list-existing-subscriptions"></a><span data-ttu-id="3e168-109">Список существующих подписок</span><span class="sxs-lookup"><span data-stu-id="3e168-109">List existing subscriptions</span></span>

<span data-ttu-id="3e168-110">Для перечисления существующих удаленных подписок на события используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3e168-110">The following syntax is used to list existing remote event subscriptions.</span></span>

``` syntax
wecutil { es | enum-subscription }
```

<span data-ttu-id="3e168-111">Если для получения имен подписок из выходных данных используется сценарий, необходимо обойти символы спецификации UTF-8 в первой строке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3e168-111">If you use a script to get the names of the subscriptions from the output, you will need to bypass the UTF-8 BOM characters in the first line of the output.</span></span> <span data-ttu-id="3e168-112">В следующем сценарии показан пример того, как можно пропустить символы спецификации.</span><span class="sxs-lookup"><span data-stu-id="3e168-112">The following script shows an example of how you might skip the BOM characters.</span></span>

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

## <a name="get-subscription-configuration"></a><span data-ttu-id="3e168-113">Получение конфигурации подписки</span><span class="sxs-lookup"><span data-stu-id="3e168-113">Get subscription configuration</span></span>

<span data-ttu-id="3e168-114">Для просмотра данных конфигурации удаленной подписки на события используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3e168-114">The following syntax is used to display remote event subscription configuration data.</span></span>

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a><span data-ttu-id="3e168-115">Получить параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="3e168-115">Get Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e168-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**</span><span class="sxs-lookup"><span data-stu-id="3e168-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-117">Строка, однозначно определяющая подписку.</span><span class="sxs-lookup"><span data-stu-id="3e168-117">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="3e168-118">Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-118">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: \* значение**\*</span><span class="sxs-lookup"><span data-stu-id="3e168-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:\*VALUE**\*</span></span>
</dt> <dd>

<span data-ttu-id="3e168-120">Значение типа, указывающее выходные данные конфигурации подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-120">A value that specifies the output of the subscription configuration data.</span></span> <span data-ttu-id="3e168-121">Может иметь *значение* "XML" или "сжатый", а по умолчанию — "сжатый".</span><span class="sxs-lookup"><span data-stu-id="3e168-121">*VALUE* can be "XML" or "Terse", and the default is "Terse".</span></span> <span data-ttu-id="3e168-122">Если *значение параметра* — "XML", выходные данные выводятся в формате "XML".</span><span class="sxs-lookup"><span data-stu-id="3e168-122">If *VALUE* is "XML", then the output is printed in "XML" format.</span></span> <span data-ttu-id="3e168-123">Если *значение параметра* — "сжатый", выходные данные выводятся в виде пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="3e168-123">If *VALUE* is "Terse", then the output is printed in name-value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *значение***</span><span class="sxs-lookup"><span data-stu-id="3e168-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-125">Значение типа, указывающее, имеет ли выходные данные формат Юникода.</span><span class="sxs-lookup"><span data-stu-id="3e168-125">A value that specifies whether the output is in Unicode format.</span></span> <span data-ttu-id="3e168-126">*Значение* может быть "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="3e168-126">*VALUE* can be "true" or "false".</span></span> <span data-ttu-id="3e168-127">Если *значение* равно true, то выходные данные имеют формат Юникода, а если *значение* — false, то выходные данные не имеют формата Юникода.</span><span class="sxs-lookup"><span data-stu-id="3e168-127">If *VALUE* is "true", then the output is in Unicode format, and if *VALUE* is "false", then the output is not in Unicode format.</span></span>

</dd> </dl>

## <a name="get-subscription-runtime-status"></a><span data-ttu-id="3e168-128">Получение состояния среды выполнения подписки</span><span class="sxs-lookup"><span data-stu-id="3e168-128">Get subscription runtime status</span></span>

<span data-ttu-id="3e168-129">Для вывода состояния среды выполнения подписки используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3e168-129">The following syntax is used to display the subscription runtime status.</span></span>

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a><span data-ttu-id="3e168-130">Получение параметров состояния</span><span class="sxs-lookup"><span data-stu-id="3e168-130">Get Status Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e168-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**</span><span class="sxs-lookup"><span data-stu-id="3e168-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-132">Строка, однозначно определяющая подписку.</span><span class="sxs-lookup"><span data-stu-id="3e168-132">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="3e168-133">Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-133">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_Источник события**</span><span class="sxs-lookup"><span data-stu-id="3e168-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-135">Значение, идентифицирующее компьютер, являющийся источником события для подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-135">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="3e168-136">Это значение может быть полным доменным именем компьютера, NetBIOS-имени или адреса IP.</span><span class="sxs-lookup"><span data-stu-id="3e168-136">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="set-subscription-configuration-information"></a><span data-ttu-id="3e168-137">Настройка сведений о конфигурации подписки</span><span class="sxs-lookup"><span data-stu-id="3e168-137">Set Subscription Configuration Information</span></span>

<span data-ttu-id="3e168-138">Следующий синтаксис используется для задания данных конфигурации подписки путем изменения параметров подписки из командной строки или с помощью XML-файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3e168-138">The following syntax is used to set subscription configuration data by changing subscription parameters from the command line or using an XML configuration file.</span></span>

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

### <a name="remarks"></a><span data-ttu-id="3e168-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e168-139">Remarks</span></span>

<span data-ttu-id="3e168-140">Если в команде **wecutil SS** указано неправильное имя пользователя или пароль, ошибки не выводятся до тех пор, пока вы не просмотрите состояние выполнения подписки с помощью команды **wecutil GR** .</span><span class="sxs-lookup"><span data-stu-id="3e168-140">When an incorrect username or password is specified in the **wecutil ss** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="set-configuration-parameters"></a><span data-ttu-id="3e168-141">Установка параметров конфигурации</span><span class="sxs-lookup"><span data-stu-id="3e168-141">Set Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e168-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**</span><span class="sxs-lookup"><span data-stu-id="3e168-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-143">Строка, однозначно определяющая подписку.</span><span class="sxs-lookup"><span data-stu-id="3e168-143">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="3e168-144">Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-144">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *конгиг \_ файл***</span><span class="sxs-lookup"><span data-stu-id="3e168-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG\_FILE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-146">Значение типа, указывающее путь к XML-файлу, содержащему сведения о конфигурации подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-146">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="3e168-147">Путь может быть абсолютным или относительным для текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="3e168-147">The path can be absolute or relative to the current directory.</span></span> <span data-ttu-id="3e168-148">Этот параметр можно использовать только с необязательными параметрами/кус и/КУП и является взаимоисключающим со всеми другими параметрами.</span><span class="sxs-lookup"><span data-stu-id="3e168-148">This parameter can only be used with the optional /cus and /cup parameters, and is mutually exclusive with all the other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *значение***</span><span class="sxs-lookup"><span data-stu-id="3e168-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-150">Значение, определяющее, следует ли включать или отключать подписку.</span><span class="sxs-lookup"><span data-stu-id="3e168-150">A value that determines whether to enable or disable the subscription.</span></span> <span data-ttu-id="3e168-151">Может иметь значение true или false.</span><span class="sxs-lookup"><span data-stu-id="3e168-151">VALUE can be true or false.</span></span> <span data-ttu-id="3e168-152">Значение по умолчанию — true, что включает подписку.</span><span class="sxs-lookup"><span data-stu-id="3e168-152">The default value is true, which enables the subscription.</span></span>

> [!Note]  
> <span data-ttu-id="3e168-153">При отключении подписки, инициированной сборщиком, источник событий переходит в неактивное состояние вместо отключения.</span><span class="sxs-lookup"><span data-stu-id="3e168-153">When you disable a collector initiated subscription, the event source becomes inactive instead of disabled.</span></span> <span data-ttu-id="3e168-154">В подписке, инициированной сборщиком, можно отключить источник событий независимо от подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-154">In a collector initiated subscription, you can disable an event source independent of the subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e168-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Описание***</span><span class="sxs-lookup"><span data-stu-id="3e168-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-156">Значение типа, указывающее описание подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-156">A value that specifies a description for the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ЕКС: *Дата и \_ время***</span><span class="sxs-lookup"><span data-stu-id="3e168-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE\_TIME***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-158">Значение типа, указывающее срок действия подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-158">A value that specifies the subscription expiration time.</span></span> <span data-ttu-id="3e168-159">*Дата \_ ВРЕМЯ* — это значение, заданное в стандартном формате XML или ISO8601: "гггг-мм-ddThh: мм: СС \[ . SSS \] \[ Z \] ", где "T" — это разделитель времени, а "Z" — время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="3e168-159">*DATE\_TIME* is a value specified in standard XML or ISO8601 date-time format: "yyyy-MM-ddThh:mm:ss\[.sss\]\[Z\]" where "T" is the time separator and "Z" indicates UTC time.</span></span> <span data-ttu-id="3e168-160">Например, если *Дата и \_ время* имеют значение "2007-01-12T01:20:00", срок действия подписки составляет 12 января 2007 01:20.</span><span class="sxs-lookup"><span data-stu-id="3e168-160">For example, if *DATE\_TIME* is "2007-01-12T01:20:00", then the subscription expiration time is January 12th, 2007, 01:20.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/Ури: *URI***</span><span class="sxs-lookup"><span data-stu-id="3e168-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-162">Значение типа, указывающее тип событий, потребляемых подпиской.</span><span class="sxs-lookup"><span data-stu-id="3e168-162">A value that specifies the type of events consumed by the subscription.</span></span> <span data-ttu-id="3e168-163">Адрес исходного компьютера события вместе с универсальным кодом ресурса (URI) однозначно определяет источник событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-163">The address of the event source computer along with the uniform resource identifier (URI) uniquely identifies the source of the events.</span></span> <span data-ttu-id="3e168-164">Строка URI используется для всех адресов источников событий в подписке.</span><span class="sxs-lookup"><span data-stu-id="3e168-164">The URI string is used for all event source addresses in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/CM: *\_ режим конфигурации***</span><span class="sxs-lookup"><span data-stu-id="3e168-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *CONFIGURATION\_MODE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-166">Значение типа, указывающее режим конфигурации подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-166">A value that specifies the configuration mode of the event subscription.</span></span> <span data-ttu-id="3e168-167">*Конфигурация \_ РЕЖИМ* может быть одной из следующих строк: "Обычная", "Custom", "минлатенци" или "MinBandwidth".</span><span class="sxs-lookup"><span data-stu-id="3e168-167">*CONFIGURATION\_MODE* can be one of the following strings: "Normal", "Custom", "MinLatency", or "MinBandwidth".</span></span> <span data-ttu-id="3e168-168">Перечисление [**\_ \_ \_ режима конфигурации подписки EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) определяет режимы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3e168-168">The [**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) enumeration defines the configuration modes.</span></span> <span data-ttu-id="3e168-169">Параметры/дм,/ДМИ,/Хи и/дмлт можно указывать, только если для режима конфигурации задано значение Custom.</span><span class="sxs-lookup"><span data-stu-id="3e168-169">The /dm, /dmi, /hi, and /dmlt parameters can only be specified if the configuration mode is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *запрос***</span><span class="sxs-lookup"><span data-stu-id="3e168-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-171">Значение типа, указывающее строку запроса для подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-171">A value that specifies the query string for the subscription.</span></span> <span data-ttu-id="3e168-172">Формат этой строки может отличаться для разных значений URI и применяться ко всем источникам событий в подписке.</span><span class="sxs-lookup"><span data-stu-id="3e168-172">The format of this string can be different for different URI values and applies to all event sources in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/Диа: *диалект***</span><span class="sxs-lookup"><span data-stu-id="3e168-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-174">Значение типа, указывающее диалект, используемый строкой запроса.</span><span class="sxs-lookup"><span data-stu-id="3e168-174">A value that specifies the dialect the query string uses.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/КФ: *Формат***</span><span class="sxs-lookup"><span data-stu-id="3e168-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-176">Значение типа, указывающее формат возвращаемых событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-176">A value that specifies the format of the returned events.</span></span> <span data-ttu-id="3e168-177">*Формат* может быть "Events" или "рендередтекст".</span><span class="sxs-lookup"><span data-stu-id="3e168-177">*FORMAT* can be "Events" or "RenderedText".</span></span> <span data-ttu-id="3e168-178">Если значение равно "Рендередтекст", то события возвращаются с помощью локализованных строк (например, строк описания событий), прикрепленных к событиям.</span><span class="sxs-lookup"><span data-stu-id="3e168-178">When the value is "RenderedText", the events are returned with the localized strings (such as event description strings) attached to the events.</span></span> <span data-ttu-id="3e168-179">По умолчанию используется значение *Format* "рендередтекст".</span><span class="sxs-lookup"><span data-stu-id="3e168-179">The default value of *FORMAT* is "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="3e168-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *языковой стандарт***</span><span class="sxs-lookup"><span data-stu-id="3e168-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-181">Значение, указывающее языковой стандарт для доставки локализованных строк в формате отображаемого текста.</span><span class="sxs-lookup"><span data-stu-id="3e168-181">A value that specifies the locale for delivery of the localized strings in rendered text format.</span></span> <span data-ttu-id="3e168-182">*Языковой стандарт* — это идентификатор культуры языка или страны, например en-US.</span><span class="sxs-lookup"><span data-stu-id="3e168-182">*LOCALE* is a language/country culture identifier, for example, "EN-us".</span></span> <span data-ttu-id="3e168-183">Этот параметр допустим только в том случае, если для параметра/КФ задано значение "Рендередтекст".</span><span class="sxs-lookup"><span data-stu-id="3e168-183">This parameter is only valid when the /cf parameter is set to "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="3e168-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ри: \[ *значение*\]**</span><span class="sxs-lookup"><span data-stu-id="3e168-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree:\[*VALUE*\]**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-185">Значение, указывающее, какие события должны быть доставлены для подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-185">A value that specifies which events are to be delivered for the subscription.</span></span> <span data-ttu-id="3e168-186">Может иметь *значение* true или false.</span><span class="sxs-lookup"><span data-stu-id="3e168-186">*VALUE* can be true or false.</span></span> <span data-ttu-id="3e168-187">Если *значение* равно true, все существующие события считываются из источников событий подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-187">When *VALUE* is true, all existing events are read from the subscription event sources.</span></span> <span data-ttu-id="3e168-188">Если *значение* равно false, доставляются только будущие (поступающие) события.</span><span class="sxs-lookup"><span data-stu-id="3e168-188">When *VALUE* is false, only future (arriving) events are delivered.</span></span> <span data-ttu-id="3e168-189">Значение по умолчанию — true, если/ри указан без значения, а значение по умолчанию — false, если/ри не задан.</span><span class="sxs-lookup"><span data-stu-id="3e168-189">The default is true when /ree is specified without a value, and the default is false if /ree is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/ЛФ: *имя файла***</span><span class="sxs-lookup"><span data-stu-id="3e168-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-191">Значение типа, указывающее локальный журнал событий, который используется для хранения событий, полученных из подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-191">A value that specifies the local event log that is used to store events received from the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/Пн: *Издатель***</span><span class="sxs-lookup"><span data-stu-id="3e168-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-193">Значение типа, указывающее имя издателя события (поставщика).</span><span class="sxs-lookup"><span data-stu-id="3e168-193">A value that specifies the event publisher (provider) name.</span></span> <span data-ttu-id="3e168-194">Он должен быть издателем, который владеет или импортирует журнал, заданный параметром/ЛФ.</span><span class="sxs-lookup"><span data-stu-id="3e168-194">It must be a publisher which owns or imports the log specified by the /lf parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/дм: *режим***</span><span class="sxs-lookup"><span data-stu-id="3e168-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-196">Значение типа, указывающее режим доставки подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-196">A value that specifies the subscription delivery mode.</span></span> <span data-ttu-id="3e168-197">*Режим* может принимать значение push или Pull.</span><span class="sxs-lookup"><span data-stu-id="3e168-197">*MODE* can be either push or pull.</span></span> <span data-ttu-id="3e168-198">Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.</span><span class="sxs-lookup"><span data-stu-id="3e168-198">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/Дми: *число***</span><span class="sxs-lookup"><span data-stu-id="3e168-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-200">Значение, указывающее максимальное количество элементов для пакетной доставки в подписке на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-200">A value that specifies the maximum number of items for batched delivery in the event subscription.</span></span> <span data-ttu-id="3e168-201">Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.</span><span class="sxs-lookup"><span data-stu-id="3e168-201">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/дмлт: *МС***</span><span class="sxs-lookup"><span data-stu-id="3e168-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-203">Значение, указывающее максимальную задержку, разрешенную для доставки пакета событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-203">A value that specifies the maximum latency allowed in delivering a batch of events.</span></span> <span data-ttu-id="3e168-204">МС — это допустимое количество миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="3e168-204">MS is the number of milliseconds allowed.</span></span> <span data-ttu-id="3e168-205">Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.</span><span class="sxs-lookup"><span data-stu-id="3e168-205">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Хи: *МС***</span><span class="sxs-lookup"><span data-stu-id="3e168-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-207">Значение, указывающее интервал пульса для подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-207">A value that specifies the heartbeat interval for the subscription.</span></span> <span data-ttu-id="3e168-208">*МС* — это количество миллисекунд, использованных в интервале.</span><span class="sxs-lookup"><span data-stu-id="3e168-208">*MS* is the number of milliseconds used in the interval.</span></span> <span data-ttu-id="3e168-209">Этот параметр допустим только в том случае, если для параметра/cm задано значение Custom.</span><span class="sxs-lookup"><span data-stu-id="3e168-209">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *транспорта***</span><span class="sxs-lookup"><span data-stu-id="3e168-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-211">Значение типа, указывающее имя транспорта, используемого для подключения к удаленному компьютеру источника событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-211">A value that specifies the name of the transport used to connect to the remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ЕСА: *\_ Источник события***</span><span class="sxs-lookup"><span data-stu-id="3e168-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT\_SOURCE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-213">Значение типа, указывающее адрес исходного компьютера события.</span><span class="sxs-lookup"><span data-stu-id="3e168-213">A value that specifies the address of an event source computer.</span></span> <span data-ttu-id="3e168-214">*Событие \_ Источник* — это строка, которая определяет компьютер источника событий с помощью полного доменного имени компьютера, NetBIOS-имени или IP адреса.</span><span class="sxs-lookup"><span data-stu-id="3e168-214">*EVENT\_SOURCE* is a string that identifies an event source computer using the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span> <span data-ttu-id="3e168-215">Этот параметр можно использовать с параметрами/ЕСЕ,/АЕС,/RES или/Ун и/up.</span><span class="sxs-lookup"><span data-stu-id="3e168-215">This parameter can be used with the /ese, /aes, /res, or /un and /up parameters.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ЕСЕ: *значение***</span><span class="sxs-lookup"><span data-stu-id="3e168-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-217">Значение, определяющее, включать или отключать источник событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-217">A value that determines whether to enable or disable an event source.</span></span> <span data-ttu-id="3e168-218">Может иметь *значение* true или false.</span><span class="sxs-lookup"><span data-stu-id="3e168-218">*VALUE* can be true or false.</span></span> <span data-ttu-id="3e168-219">Значение по умолчанию — true, что включает источник события.</span><span class="sxs-lookup"><span data-stu-id="3e168-219">The default value is true, which enables the event source.</span></span> <span data-ttu-id="3e168-220">Этот параметр используется только в том случае, если используется параметр/ЕСА.</span><span class="sxs-lookup"><span data-stu-id="3e168-220">This parameter is only used if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-221"><span id="_aes"></span><span id="_AES"></span>**/аес**</span><span class="sxs-lookup"><span data-stu-id="3e168-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-222">Значение, добавляющее источник событий, заданный параметром/ЕСА, если источник события еще не является частью подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-222">A value that adds the event source specified by the /esa parameter if the event source is not already part of the event subscription.</span></span> <span data-ttu-id="3e168-223">Если компьютер, указанный параметром/ЕСА, уже входит в подписку, отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3e168-223">If the computer specified by the /esa parameter is already a part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="3e168-224">Этот параметр разрешен только в том случае, если используется параметр/ЕСА.</span><span class="sxs-lookup"><span data-stu-id="3e168-224">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-225"><span id="_res"></span><span id="_RES"></span>**/RES**</span><span class="sxs-lookup"><span data-stu-id="3e168-225"><span id="_res"></span><span id="_RES"></span>**/res**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-226">Значение, которое удаляет источник события, указанный параметром/ЕСА, если источник события уже является частью подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-226">A value that removes the event source specified by the /esa parameter if the event source is already part of the event subscription.</span></span> <span data-ttu-id="3e168-227">Если компьютер, указанный параметром/ЕСА, не входит в подписку, отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3e168-227">If the computer specified by the /esa parameter is not part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="3e168-228">Этот параметр разрешен только в том случае, если используется параметр/ЕСА.</span><span class="sxs-lookup"><span data-stu-id="3e168-228">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/Ун: *имя пользователя***</span><span class="sxs-lookup"><span data-stu-id="3e168-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-230">Значение, указывающее имя пользователя, используемое в учетных данных для подключения к источнику событий, указанному в параметре/ЕСА.</span><span class="sxs-lookup"><span data-stu-id="3e168-230">A value that specifies the user name used in the credentials to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="3e168-231">Этот параметр разрешен только в том случае, если используется параметр/ЕСА.</span><span class="sxs-lookup"><span data-stu-id="3e168-231">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/Up: *пароль***</span><span class="sxs-lookup"><span data-stu-id="3e168-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-233">Значение типа, указывающее пароль для имени пользователя, указанного в параметре/ун.</span><span class="sxs-lookup"><span data-stu-id="3e168-233">A value that specifies the password for the user name specified in the /un parameter.</span></span> <span data-ttu-id="3e168-234">Учетные данные имени пользователя и пароля используются для подключения к источнику событий, указанному в параметре/ЕСА.</span><span class="sxs-lookup"><span data-stu-id="3e168-234">The user name and password credentials are used to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="3e168-235">Этот параметр разрешен только в том случае, если используется параметр/ун.</span><span class="sxs-lookup"><span data-stu-id="3e168-235">This parameter is allowed only if the /un parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *транспортпорт***</span><span class="sxs-lookup"><span data-stu-id="3e168-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-237">Значение, указывающее номер порта, используемый транспортом при соединении с удаленным компьютером источника событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-237">A value that specifies the port number used by the transport when connecting to a remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/ХН: *имя***</span><span class="sxs-lookup"><span data-stu-id="3e168-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-239">Значение типа, указывающее DNS-имя локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="3e168-239">A value that specifies the DNS name of the local computer.</span></span> <span data-ttu-id="3e168-240">Это имя используется удаленными источниками событий для отправки событий обратно и должно использоваться только для принудительных подписок.</span><span class="sxs-lookup"><span data-stu-id="3e168-240">This name is used by remote event sources to push back events and must be used for push subscriptions only.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/КТ: *тип***</span><span class="sxs-lookup"><span data-stu-id="3e168-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-242">Значение типа, указывающее тип учетных данных, используемый для доступа к удаленным источникам событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-242">A value that specifies the credential type used for accessing remote event sources.</span></span> <span data-ttu-id="3e168-243">*Тип* может быть "default", "Negotiate", "Digest", "Basic" или "LocalMachine".</span><span class="sxs-lookup"><span data-stu-id="3e168-243">*TYPE* can be "default", "negotiate", "digest", "basic", or "localmachine".</span></span> <span data-ttu-id="3e168-244">Значение по умолчанию — "по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="3e168-244">The default is "default".</span></span> <span data-ttu-id="3e168-245">Эти значения определены в перечислении [**\_ \_ \_ типа учетных данных подписки EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .</span><span class="sxs-lookup"><span data-stu-id="3e168-245">These values are defined in the [**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Кун: *имя пользователя***</span><span class="sxs-lookup"><span data-stu-id="3e168-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-247">Значение, устанавливающее общие учетные данные пользователя, используемые для источников событий, не имеющих собственных учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e168-247">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span>

> [!Note]  
> <span data-ttu-id="3e168-248">Если этот параметр используется с параметром/c, то параметры имени пользователя и пароля для отдельных источников событий из файла конфигурации игнорируются.</span><span class="sxs-lookup"><span data-stu-id="3e168-248">If this parameter is used with the /c option, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="3e168-249">Если вы хотите использовать разные учетные данные для определенного источника событий, это значение можно переопределить, указав параметры/Ун и/up для определенного источника события в командной строке другой команды Set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="3e168-249">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e168-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/КУП: *пароль***</span><span class="sxs-lookup"><span data-stu-id="3e168-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-251">Значение, которое задает пароль пользователя для учетных данных общего пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e168-251">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="3e168-252">Если для параметра *Password* задано значение \* (звездочка), то пароль считывается из консоли.</span><span class="sxs-lookup"><span data-stu-id="3e168-252">When *PASSWORD* is set to \* (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="3e168-253">Этот параметр допустим только в том случае, если указан параметр/кун.</span><span class="sxs-lookup"><span data-stu-id="3e168-253">This option is only valid when the /cun parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ИКА: *отпечатки***</span><span class="sxs-lookup"><span data-stu-id="3e168-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *THUMBPRINTS***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-255">Значение, задающее список отпечаток сертификата издателя, в списке с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="3e168-255">A value that sets the list of issuer certificate thumb prints, in a comma-separated list.</span></span>

> [!Note]  
> <span data-ttu-id="3e168-256">Этот параметр относится только к исходным подпискам, инициированным источником.</span><span class="sxs-lookup"><span data-stu-id="3e168-256">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e168-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/АС: *разрешено***</span><span class="sxs-lookup"><span data-stu-id="3e168-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-258">Значение, которое задает разделенный запятыми список строк, указывающий DNS-имена компьютеров, не являющихся доменами, которым разрешено инициировать подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-258">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are allowed to initiate subscriptions.</span></span> <span data-ttu-id="3e168-259">Имена можно указать с помощью подстановочных знаков, например " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="3e168-259">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="3e168-260">По умолчанию этот список пустой.</span><span class="sxs-lookup"><span data-stu-id="3e168-260">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="3e168-261">Этот параметр относится только к исходным подпискам, инициированным источником.</span><span class="sxs-lookup"><span data-stu-id="3e168-261">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e168-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ДС: *запрещено***</span><span class="sxs-lookup"><span data-stu-id="3e168-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-263">Значение, которое задает разделенный запятыми список строк, указывающий DNS-имена недоменных компьютеров, для которых запрещено инициировать подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-263">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are not allowed to initiate subscriptions.</span></span> <span data-ttu-id="3e168-264">Имена можно указать с помощью подстановочных знаков, например " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="3e168-264">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="3e168-265">По умолчанию этот список пустой.</span><span class="sxs-lookup"><span data-stu-id="3e168-265">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="3e168-266">Этот параметр относится только к исходным подпискам, инициированным источником.</span><span class="sxs-lookup"><span data-stu-id="3e168-266">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e168-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/АДК: *SDDL***</span><span class="sxs-lookup"><span data-stu-id="3e168-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-268">Значение, которое задает строку в формате SDDL, указывающую, какие компьютеры домена разрешены или запрещены для инициирования подписок.</span><span class="sxs-lookup"><span data-stu-id="3e168-268">A value that sets a string, in SDDL format, that specifies which domain computers are allowed or not allowed to initiate subscriptions.</span></span> <span data-ttu-id="3e168-269">Значение по умолчанию — разрешить всем компьютерам домена инициировать подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-269">The default is to allow all domain computers to initiate subscriptions.</span></span>

> [!Note]  
> <span data-ttu-id="3e168-270">Этот параметр относится только к исходным подпискам, инициированным источником.</span><span class="sxs-lookup"><span data-stu-id="3e168-270">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> </dl>

## <a name="create-a-new-subscription"></a><span data-ttu-id="3e168-271">Создание новой подписки</span><span class="sxs-lookup"><span data-stu-id="3e168-271">Create a New Subscription</span></span>

<span data-ttu-id="3e168-272">Для создания подписки на события на удаленном компьютере используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3e168-272">The following syntax is used to create an event subscription for events on a remote computer.</span></span>

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a><span data-ttu-id="3e168-273">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e168-273">Remarks</span></span>

<span data-ttu-id="3e168-274">Если в команде **wecutil CS** указано неправильное имя пользователя или пароль, ошибки не выводятся до тех пор, пока вы не просмотрите состояние выполнения подписки с помощью команды **wecutil GR** .</span><span class="sxs-lookup"><span data-stu-id="3e168-274">When an incorrect username or password is specified in the **wecutil cs** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="creation-parameters"></a><span data-ttu-id="3e168-275">Параметры создания</span><span class="sxs-lookup"><span data-stu-id="3e168-275">Creation Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e168-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**\_файл конфигурации**</span><span class="sxs-lookup"><span data-stu-id="3e168-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**CONFIGURATION\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-277">Значение типа, указывающее путь к XML-файлу, содержащему сведения о конфигурации подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-277">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="3e168-278">Путь может быть абсолютным или относительным для текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="3e168-278">The path can be absolute or relative to the current directory.</span></span>

<span data-ttu-id="3e168-279">Следующий код XML является примером файла конфигурации подписки, который создает подписку, инициированную сборщиком, для перенаправления событий из журнала событий приложений удаленного компьютера в журнал ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="3e168-279">The following XML is an example of a subscription configuration file that creates a collector initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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



<span data-ttu-id="3e168-280">Следующий код XML является примером файла конфигурации подписки, который создает созданную источником подписку для перенаправления событий из журнала событий приложений удаленного компьютера в журнал ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="3e168-280">The following XML is an example of a subscription configuration file that creates a source initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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
> <span data-ttu-id="3e168-281">При создании исходной инициированной подписки, если **алловедсаурцедомаинкомпутерс**, **алловедсаурценондомаинкомпутерс** / **иссуеркалист**, **алловедсубжектлист** и **DeniedSubjectList** все пусты, будет использоваться значение по умолчанию для **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; Общедоступный;;; NS) ".</span><span class="sxs-lookup"><span data-stu-id="3e168-281">When creating a source initiated subscription, if **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers**/**IssuerCAList**, **AllowedSubjectList**, and **DeniedSubjectList** are all empty, then a default will be provided for **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)".</span></span> <span data-ttu-id="3e168-282">По умолчанию SDDL предоставляет членам группы домена "компьютеры домена", а также группы локальных сетевых служб (для локального сервера пересылки) возможность создавать события для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-282">This SDDL default grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e168-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Кун: *имя пользователя***</span><span class="sxs-lookup"><span data-stu-id="3e168-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-284">Значение, устанавливающее общие учетные данные пользователя, используемые для источников событий, не имеющих собственных учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e168-284">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span> <span data-ttu-id="3e168-285">Это значение применяется только к подпискам, инициированным сборщиком.</span><span class="sxs-lookup"><span data-stu-id="3e168-285">This value applies to collector initiated subscriptions only.</span></span>

> [!Note]  
> <span data-ttu-id="3e168-286">Если этот параметр указан, то параметры имени пользователя и пароля для отдельных источников событий из файла конфигурации игнорируются.</span><span class="sxs-lookup"><span data-stu-id="3e168-286">If this parameter is specified, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="3e168-287">Если вы хотите использовать разные учетные данные для определенного источника событий, это значение можно переопределить, указав параметры/Ун и/up для определенного источника события в командной строке другой команды Set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="3e168-287">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e168-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/КУП: *пароль***</span><span class="sxs-lookup"><span data-stu-id="3e168-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-289">Значение, которое задает пароль пользователя для учетных данных общего пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e168-289">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="3e168-290">Если для параметра *Password* задано значение " \* " (звездочка), то пароль считывается из консоли.</span><span class="sxs-lookup"><span data-stu-id="3e168-290">When *PASSWORD* is set to "\*" (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="3e168-291">Этот параметр допустим только в том случае, если указан параметр/кун.</span><span class="sxs-lookup"><span data-stu-id="3e168-291">This option is only valid when the /cun parameter is specified.</span></span>

</dd> </dl>

## <a name="delete-a-subscription"></a><span data-ttu-id="3e168-292">Удаление подписки</span><span class="sxs-lookup"><span data-stu-id="3e168-292">Delete a Subscription</span></span>

<span data-ttu-id="3e168-293">Для удаления подписки на события используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3e168-293">The following syntax is used to delete an event subscription.</span></span>

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a><span data-ttu-id="3e168-294">Параметры удаления</span><span class="sxs-lookup"><span data-stu-id="3e168-294">Deletion Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e168-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**</span><span class="sxs-lookup"><span data-stu-id="3e168-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-296">Строка, однозначно определяющая подписку.</span><span class="sxs-lookup"><span data-stu-id="3e168-296">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="3e168-297">Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-297">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="3e168-298">Подписка, указанная в этом параметре, будет удалена.</span><span class="sxs-lookup"><span data-stu-id="3e168-298">The subscription identified in this parameter will be deleted.</span></span>

</dd> </dl>

## <a name="retry-a-subscription"></a><span data-ttu-id="3e168-299">Повтор подписки</span><span class="sxs-lookup"><span data-stu-id="3e168-299">Retry a subscription</span></span>

<span data-ttu-id="3e168-300">Следующий синтаксис используется для повторного выполнения неактивной подписки путем попытки повторной активации всех или указанных источников событий путем установки соединения с каждым источником событий и отправки запроса на удаленную подписку в источник событий.</span><span class="sxs-lookup"><span data-stu-id="3e168-300">The following syntax is used to retry an inactive subscription by attempting to reactivate all or specified event sources by establishing a connection to each event source and sending a remote subscription request to the event source.</span></span> <span data-ttu-id="3e168-301">Отключенные источники событий не повторяются.</span><span class="sxs-lookup"><span data-stu-id="3e168-301">Disabled event sources are not retried.</span></span>

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a><span data-ttu-id="3e168-302">Параметры повтора</span><span class="sxs-lookup"><span data-stu-id="3e168-302">Retry Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e168-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_идентификатор подписки**</span><span class="sxs-lookup"><span data-stu-id="3e168-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-304">Строка, однозначно определяющая подписку.</span><span class="sxs-lookup"><span data-stu-id="3e168-304">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="3e168-305">Этот идентификатор указан в элементе **SubscriptionId** в XML-файле конфигурации, используемом для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="3e168-305">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="3e168-306">Подписка, указанная в этом параметре, будет предпринята повторно.</span><span class="sxs-lookup"><span data-stu-id="3e168-306">The subscription identified in this parameter will be retried.</span></span>

</dd> <dt>

<span data-ttu-id="3e168-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_Источник события**</span><span class="sxs-lookup"><span data-stu-id="3e168-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="3e168-308">Значение, идентифицирующее компьютер, являющийся источником события для подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3e168-308">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="3e168-309">Это значение может быть полным доменным именем компьютера, NetBIOS-имени или адреса IP.</span><span class="sxs-lookup"><span data-stu-id="3e168-309">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a><span data-ttu-id="3e168-310">Настройка службы сборщика событий Windows</span><span class="sxs-lookup"><span data-stu-id="3e168-310">Configure the Windows Event Collector Service</span></span>

<span data-ttu-id="3e168-311">Следующий синтаксис используется для настройки службы сборщика событий Windows для обеспечения возможности создания и поддержания подписок на события при перезагрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="3e168-311">The following syntax is used to configure the Windows Event Collector service to ensure event subscriptions can be created and sustained through computer restarts.</span></span> <span data-ttu-id="3e168-312">Сюда входит следующая процедура:</span><span class="sxs-lookup"><span data-stu-id="3e168-312">This includes the following procedure:</span></span>

<span data-ttu-id="3e168-313">**Настройка службы сборщика событий Windows**</span><span class="sxs-lookup"><span data-stu-id="3e168-313">**To configure the Windows Event Collector service**</span></span>

1.  <span data-ttu-id="3e168-314">Включите канал ForwardedEvents, если он отключен.</span><span class="sxs-lookup"><span data-stu-id="3e168-314">Enable the ForwardedEvents channel if it is disabled.</span></span>
2.  <span data-ttu-id="3e168-315">Задержка запуска службы сборщика событий Windows.</span><span class="sxs-lookup"><span data-stu-id="3e168-315">Delay the start of the Windows Event Collector service.</span></span>
3.  <span data-ttu-id="3e168-316">Запустите службу сборщика событий Windows, если она не запущена.</span><span class="sxs-lookup"><span data-stu-id="3e168-316">Start the Windows Event Collector service if it is not running.</span></span>

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a><span data-ttu-id="3e168-317">Настройка параметров сборщика событий</span><span class="sxs-lookup"><span data-stu-id="3e168-317">Configure Event Collector Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e168-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *значение***</span><span class="sxs-lookup"><span data-stu-id="3e168-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="3e168-319">Значение, определяющее, будет ли команда быстрой настройки запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3e168-319">A value that determines whether the quick-config command will prompt for confirmation.</span></span> <span data-ttu-id="3e168-320">Может иметь значение true или false.</span><span class="sxs-lookup"><span data-stu-id="3e168-320">VALUE can be true or false.</span></span> <span data-ttu-id="3e168-321">Если значение — true, команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3e168-321">If VALUE is true, then the command will prompt for confirmation.</span></span> <span data-ttu-id="3e168-322">Значением по умолчанию является false.</span><span class="sxs-lookup"><span data-stu-id="3e168-322">The default value is false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e168-323">Требования</span><span class="sxs-lookup"><span data-stu-id="3e168-323">Requirements</span></span>



| <span data-ttu-id="3e168-324">Требование</span><span class="sxs-lookup"><span data-stu-id="3e168-324">Requirement</span></span> | <span data-ttu-id="3e168-325">Значение</span><span class="sxs-lookup"><span data-stu-id="3e168-325">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3e168-326">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e168-326">Minimum supported client</span></span><br/> | <span data-ttu-id="3e168-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e168-327">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3e168-328">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e168-328">Minimum supported server</span></span><br/> | <span data-ttu-id="3e168-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e168-329">Windows Server 2008</span></span><br/> |



 

 





