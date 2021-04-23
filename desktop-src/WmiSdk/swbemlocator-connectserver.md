---
description: Подключается к пространству имен на компьютере, указанном в параметре Стрсервер.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: SWbemLocator. Коннектсервер, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693590"
---
# <a name="swbemlocatorconnectserver-method"></a><span data-ttu-id="963c1-103">SWbemLocator. Коннектсервер, метод</span><span class="sxs-lookup"><span data-stu-id="963c1-103">SWbemLocator.ConnectServer method</span></span>

<span data-ttu-id="963c1-104">Метод **коннектсервер** объекта [**SWbemLocator**](swbemlocator.md) подключается к пространству имен на компьютере, указанном в параметре *стрсервер* .</span><span class="sxs-lookup"><span data-stu-id="963c1-104">The **ConnectServer** method of the [**SWbemLocator**](swbemlocator.md) object connects to the namespace on the computer that is specified in the *strServer* parameter.</span></span> <span data-ttu-id="963c1-105">Конечный компьютер может быть либо локальным, либо удаленным, но на нем должен быть установлен инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="963c1-105">The target computer can be either local or remote, but it must have WMI installed.</span></span> <span data-ttu-id="963c1-106">Примеры и сравнение с типом моникера Connection см. в разделе [Создание скрипта WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="963c1-106">For examples and a comparison with the moniker type of connection, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

<span data-ttu-id="963c1-107">Начиная с Windows Vista, **SWbemLocator. коннектсервер** может подключаться к компьютерам с IPv6 с помощью IPv6-адреса в параметре *стрсервер* .</span><span class="sxs-lookup"><span data-stu-id="963c1-107">Starting with Windows Vista, **SWbemLocator.ConnectServer** can connect with computers running IPv6 using an IPv6 address in the *strServer* parameter.</span></span> <span data-ttu-id="963c1-108">Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="963c1-108">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="963c1-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="963c1-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="963c1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="963c1-110">Syntax</span></span>


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="963c1-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="963c1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963c1-112">*стрсервер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-112">*strServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c1-113">Имя компьютера, к которому выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="963c1-113">Computer name to which you are connecting.</span></span> <span data-ttu-id="963c1-114">Если удаленный компьютер находится в домене, отличном от домена, в котором выполняется вход, используйте полное имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="963c1-114">If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.</span></span> <span data-ttu-id="963c1-115">Если этот параметр не предоставлен, по умолчанию вызывается локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="963c1-115">If you do not provide this parameter, the call defaults to the local computer.</span></span>

<span data-ttu-id="963c1-116">Пример: `server1.network.fabrikam`</span><span class="sxs-lookup"><span data-stu-id="963c1-116">Example: `server1.network.fabrikam`</span></span>

<span data-ttu-id="963c1-117">В этом параметре также можно использовать IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="963c1-117">You also can use an IP address in this parameter.</span></span> <span data-ttu-id="963c1-118">Если IP-адрес имеет формат IPv6, на целевом компьютере должен быть установлен протокол IPv6.</span><span class="sxs-lookup"><span data-stu-id="963c1-118">If the IP address is in IPv6 format, the target computer must be running IPv6.</span></span> <span data-ttu-id="963c1-119">Адрес в IPv4 выглядит следующим образом: `123.123.123.123`</span><span class="sxs-lookup"><span data-stu-id="963c1-119">An address in IPv4 looks like `123.123.123.123`</span></span>

<span data-ttu-id="963c1-120">IP-адрес в формате IPv6 выглядит следующим образом: `2010:836B:4179::836B:4179`</span><span class="sxs-lookup"><span data-stu-id="963c1-120">An IP address in IPv6 format looks like `2010:836B:4179::836B:4179`</span></span>

<span data-ttu-id="963c1-121">Дополнительные сведения о DNS и IPv4 см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="963c1-121">For more information on DNS and IPv4, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-122">*стрнамеспаце* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-122">*strNamespace* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c1-123">Строка, указывающая пространство имен, в котором вы входите в систему.</span><span class="sxs-lookup"><span data-stu-id="963c1-123">String that specifies the namespace to which you log on.</span></span> <span data-ttu-id="963c1-124">Например, чтобы войти в корневое \\ пространство имен по умолчанию, используйте корневую папку \\ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="963c1-124">For example, to log on to the root\\default namespace, use root\\default.</span></span> <span data-ttu-id="963c1-125">Если этот параметр не указан, по умолчанию используется пространство имен, настроенное в качестве пространства имен по умолчанию для сценариев.</span><span class="sxs-lookup"><span data-stu-id="963c1-125">If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting.</span></span> <span data-ttu-id="963c1-126">Дополнительные сведения см. [в разделе Создание приложения WMI или скрипта](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="963c1-126">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

<span data-ttu-id="963c1-127">Пример: "root \\ CIMV2"</span><span class="sxs-lookup"><span data-stu-id="963c1-127">Example: "root\\CIMV2"</span></span>

</dd> <dt>

<span data-ttu-id="963c1-128">*strUser* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-128">*strUser* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c1-129">Имя пользователя, используемое для подключения.</span><span class="sxs-lookup"><span data-stu-id="963c1-129">User name to use to connect.</span></span> <span data-ttu-id="963c1-130">Строка может иметь форму либо имени пользователя, либо доменного имени пользователя \\ .</span><span class="sxs-lookup"><span data-stu-id="963c1-130">The string can be in the form of either a user name or a Domain\\Username.</span></span> <span data-ttu-id="963c1-131">Оставьте этот параметр пустым, чтобы использовать текущий контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="963c1-131">Leave this parameter blank to use the current security context.</span></span> <span data-ttu-id="963c1-132">Параметр *strUser* следует использовать только с соединениями с удаленными серверами WMI.</span><span class="sxs-lookup"><span data-stu-id="963c1-132">The *strUser* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="963c1-133">При попытке указать *strUser* для ЛОКАЛЬНОГО подключения WMI попытка подключения завершится неудачей.</span><span class="sxs-lookup"><span data-stu-id="963c1-133">If you attempt to specify *strUser* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="963c1-134">Если используется проверка подлинности Kerberos, то имя пользователя и пароль, указанные в параметре *strUser* и *стрпассворд* , не могут быть перехвачены в сети.</span><span class="sxs-lookup"><span data-stu-id="963c1-134">If Kerberos authentication is in use, then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on a network.</span></span> <span data-ttu-id="963c1-135">Для указания *strUser* можно использовать формат имени участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="963c1-135">You can use the UPN format to specify the *strUser*.</span></span>

<span data-ttu-id="963c1-136">Пример: "имя_домена \\ имя_пользователя"</span><span class="sxs-lookup"><span data-stu-id="963c1-136">Example: "DomainName\\UserName"</span></span>

> [!Note]  
> <span data-ttu-id="963c1-137">Если домен указан в *страусорити*, то этот домен не должен указываться здесь.</span><span class="sxs-lookup"><span data-stu-id="963c1-137">If a domain is specified in *strAuthority*, then the domain must not be specified here.</span></span> <span data-ttu-id="963c1-138">Указание домена в обоих параметрах приводит к ошибке недопустимого параметра.</span><span class="sxs-lookup"><span data-stu-id="963c1-138">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="963c1-139">*стрпассворд* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-139">*strPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c1-140">Строка, указывающая пароль, используемый при попытке подключения.</span><span class="sxs-lookup"><span data-stu-id="963c1-140">String that specifies the password to use when attempting to connect.</span></span> <span data-ttu-id="963c1-141">Чтобы использовать текущий контекст безопасности, оставьте параметр пустым.</span><span class="sxs-lookup"><span data-stu-id="963c1-141">Leave the parameter blank to use the current security context.</span></span> <span data-ttu-id="963c1-142">Параметр *стрпассворд* следует использовать только с соединениями с удаленными серверами WMI.</span><span class="sxs-lookup"><span data-stu-id="963c1-142">The *strPassword* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="963c1-143">При попытке указать *стрпассворд* для ЛОКАЛЬНОГО подключения WMI попытка подключения завершится неудачей.</span><span class="sxs-lookup"><span data-stu-id="963c1-143">If you attempt to specify *strPassword* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="963c1-144">Если используется проверка подлинности Kerberos, то имя пользователя и пароль, указанные в параметре *strUser* и *стрпассворд* , не могут быть перехвачены в сети.</span><span class="sxs-lookup"><span data-stu-id="963c1-144">If Kerberos authentication is in use then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on the network.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-145">*стрлокале* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-145">*strLocale* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c1-146">Строка, указывающая код локализации.</span><span class="sxs-lookup"><span data-stu-id="963c1-146">String that specifies the localization code.</span></span> <span data-ttu-id="963c1-147">Если вы хотите использовать текущий языковой стандарт, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="963c1-147">If you want to use the current locale, leave it blank.</span></span> <span data-ttu-id="963c1-148">Если значение не пустое, этот параметр должен быть строкой, указывающей предпочтительный языковой стандарт, в который должны быть извлечены сведения.</span><span class="sxs-lookup"><span data-stu-id="963c1-148">If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved.</span></span> <span data-ttu-id="963c1-149">Для идентификаторов языковых стандартов Майкрософт формат строки — MS \_ XXXX, где XXXX — строка в шестнадцатеричной форме, указывающая код языка.</span><span class="sxs-lookup"><span data-stu-id="963c1-149">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="963c1-150">Например, американский английский будет выглядеть как "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="963c1-150">For example, American English would appear as "MS\_409".</span></span>

</dd> <dt>

<span data-ttu-id="963c1-151">*страусорити* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-151">*strAuthority* \[in, optional\]</span></span>
</dt> <dd>

<dt>

<span data-ttu-id="963c1-152">""</span><span class="sxs-lookup"><span data-stu-id="963c1-152">""</span></span>
</dt> <dd>

<span data-ttu-id="963c1-153">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="963c1-153">This parameter is optional.</span></span> <span data-ttu-id="963c1-154">Однако, если он указан, можно использовать только Kerberos или Нтлмдомаин.</span><span class="sxs-lookup"><span data-stu-id="963c1-154">However, if it is specified, only Kerberos or NTLMDomain can be used.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-155">Проверк</span><span class="sxs-lookup"><span data-stu-id="963c1-155">Kerberos:</span></span>
</dt> <dd>

<span data-ttu-id="963c1-156">Если параметр *страусорити* начинается со строки "Kerberos:", используется проверка подлинности Kerberos и этот параметр должен содержать имя участника Kerberos.</span><span class="sxs-lookup"><span data-stu-id="963c1-156">If the *strAuthority* parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name.</span></span> <span data-ttu-id="963c1-157">Имя участника Kerberos указывается как Kerberos:*domain*, например, `Kerberos:fabrikam` где `fabrikam` — это сервер, к которому выполняется попытка подключения.</span><span class="sxs-lookup"><span data-stu-id="963c1-157">The Kerberos principal name is specified as Kerberos:*domain*, such as `Kerberos:fabrikam` where `fabrikam` is the server to which you are attempting to connect.</span></span>

<span data-ttu-id="963c1-158">Пример: "Kerberos: домен"</span><span class="sxs-lookup"><span data-stu-id="963c1-158">Example: "Kerberos:DOMAIN"</span></span>

</dd> <dt>

<span data-ttu-id="963c1-159">Нтлмдомаин:</span><span class="sxs-lookup"><span data-stu-id="963c1-159">NTLMDomain:</span></span>
</dt> <dd>

<span data-ttu-id="963c1-160">Чтобы использовать проверку подлинности NT LAN Manager (NTLM), необходимо указать ее как Нтлмдомаин:*domain*, например, `NTLMDomain:fabrikam` где `fabrikam` — это имя домена.</span><span class="sxs-lookup"><span data-stu-id="963c1-160">To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:*domain*, such as `NTLMDomain:fabrikam` where `fabrikam` is the name of the domain.</span></span>

<span data-ttu-id="963c1-161">Пример: "Нтлмдомаин: DOMAIN"</span><span class="sxs-lookup"><span data-stu-id="963c1-161">Example: "NTLMDomain:DOMAIN"</span></span>

</dd> </dl>

<span data-ttu-id="963c1-162">Если оставить этот параметр пустым, операционная система согласовывается с COM, чтобы определить, используется ли проверка подлинности NTLM или Kerberos.</span><span class="sxs-lookup"><span data-stu-id="963c1-162">If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used.</span></span> <span data-ttu-id="963c1-163">Этот параметр следует использовать только с соединениями с удаленными серверами WMI.</span><span class="sxs-lookup"><span data-stu-id="963c1-163">This parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="963c1-164">При попытке задать центр для локального WMI-подключения произойдет сбой попытки подключения.</span><span class="sxs-lookup"><span data-stu-id="963c1-164">If you attempt to set the authority for a local WMI connection, the connection attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="963c1-165">Если домен указан в параметре *strUser*, который является предпочтительным расположением, то его не следует указывать здесь.</span><span class="sxs-lookup"><span data-stu-id="963c1-165">If the domain is specified in *strUser*, which is the preferred location, then it must not be specified here.</span></span> <span data-ttu-id="963c1-166">Указание домена в обоих параметрах приводит к ошибке недопустимого параметра.</span><span class="sxs-lookup"><span data-stu-id="963c1-166">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="963c1-167">*исекуритифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-167">*iSecurityFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c1-168">Используется для передачи значений флагов в **коннектсервер**.</span><span class="sxs-lookup"><span data-stu-id="963c1-168">Used to pass flag values to **ConnectServer**.</span></span>

<dt>

<span data-ttu-id="963c1-169">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="963c1-169">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="963c1-170">Значение 0 для этого параметра приводит к возврату из вызова **коннектсервер** только после установки соединения с сервером.</span><span class="sxs-lookup"><span data-stu-id="963c1-170">A value of 0 for this parameter causes the call to **ConnectServer** to return only after the connection to the server is established.</span></span> <span data-ttu-id="963c1-171">Это может привести к тому, что программа перестанет отвечать на запросы в неопределенное время, если не удается установить соединение.</span><span class="sxs-lookup"><span data-stu-id="963c1-171">This could cause your program to stop responding indefinitely if the connection cannot be established.</span></span>

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span data-ttu-id="963c1-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>Вбемконнектфлагусемаксваит \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="963c1-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>\*\*\*\*wbemConnectFlagUseMaxWait\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="963c1-173">Вызов **коннектсервер** гарантированно возвращается в течение 2 минут или меньше.</span><span class="sxs-lookup"><span data-stu-id="963c1-173">The **ConnectServer** call is guaranteed to return in 2 minutes or less.</span></span> <span data-ttu-id="963c1-174">Используйте этот флаг, чтобы программа из прекращение не отвечала на неопределенное время, если не удается установить соединение.</span><span class="sxs-lookup"><span data-stu-id="963c1-174">Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="963c1-175">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="963c1-175">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963c1-176">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="963c1-176">Typically, this is undefined.</span></span> <span data-ttu-id="963c1-177">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="963c1-177">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="963c1-178">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="963c1-178">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963c1-179">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="963c1-179">Return value</span></span>

<span data-ttu-id="963c1-180">В случае успеха Инструментарий WMI возвращает объект [**SwbemServices**](swbemservices.md) , привязанный к пространству имен, указанному в *стрнамеспаце* на компьютере, указанном в *стрсервер*.</span><span class="sxs-lookup"><span data-stu-id="963c1-180">If successful, WMI returns an [**SWbemServices**](swbemservices.md) object that is bound to the namespace that is specified in *strNamespace* on the computer that is specified in *strServer*.</span></span>

## <a name="error-codes"></a><span data-ttu-id="963c1-181">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="963c1-181">Error codes</span></span>

<span data-ttu-id="963c1-182">После завершения метода **коннектсервер** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="963c1-182">After the completion of the **ConnectServer** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="963c1-183">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="963c1-183">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="963c1-184">Текущее или указанное имя пользователя и пароль не были допустимыми или разрешены для создания соединения.</span><span class="sxs-lookup"><span data-stu-id="963c1-184">The current or specified user name and password were not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-185">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="963c1-185">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="963c1-186">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="963c1-186">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-187">**вбемерринвалиднамеспаце** -2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="963c1-187">**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)</span></span>
</dt> <dd>

<span data-ttu-id="963c1-188">Указанное пространство имен не существует на сервере.</span><span class="sxs-lookup"><span data-stu-id="963c1-188">The specified namespace did not exist on the server.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-189">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="963c1-189">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="963c1-190">Указан недопустимый параметр, или не удалось выполнить синтаксический анализ пространства имен.</span><span class="sxs-lookup"><span data-stu-id="963c1-190">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-191">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="963c1-191">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="963c1-192">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="963c1-192">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="963c1-193">**вбемерртранспортфаилуре** -2147749909</span><span class="sxs-lookup"><span data-stu-id="963c1-193">**wbemErrTransportFailure** - 2147749909</span></span>
</dt> <dd>

<span data-ttu-id="963c1-194">Произошла сетевая ошибка, препятствующая нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="963c1-194">A networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="963c1-195">Комментарии</span><span class="sxs-lookup"><span data-stu-id="963c1-195">Remarks</span></span>

<span data-ttu-id="963c1-196">Метод **коннектсервер** часто используется при подключении к учетной записи с другими учетными данными пользователя и пароля на удаленном компьютере, так как в строке [моникера](constructing-a-moniker-string.md) нельзя указать другой пароль.</span><span class="sxs-lookup"><span data-stu-id="963c1-196">The **ConnectServer** method is often used when connecting to an account with a different username and password credentials on a remote computer because you cannot specify a different password in a [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="963c1-197">Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="963c1-197">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="963c1-198">Использование IPv4-адреса для подключения к удаленному серверу может привести к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="963c1-198">Using an IPv4 address to connect to a remote server may result in unexpected behavior.</span></span> <span data-ttu-id="963c1-199">Вероятная причина — устаревшие записи DNS в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="963c1-199">The likely cause is stale DNS entries in your environment.</span></span> <span data-ttu-id="963c1-200">В таких случаях будет использоваться устаревшая запись PTR для компьютера с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="963c1-200">In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results.</span></span> <span data-ttu-id="963c1-201">Чтобы избежать такого поведения, перед вызовом Коннектсервер можно добавить точку (".") к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="963c1-201">To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer.</span></span> <span data-ttu-id="963c1-202">Это приводит к сбою уточняющего запроса DNS, но может привести к успешному выполнению вызова **коннектсервер** на нужном компьютере.</span><span class="sxs-lookup"><span data-stu-id="963c1-202">This causes the reverse DNS lookup to fail, but may allow the **ConnectServer** call to succeed on the correct machine.</span></span>

## <a name="examples"></a><span data-ttu-id="963c1-203">Примеры</span><span class="sxs-lookup"><span data-stu-id="963c1-203">Examples</span></span>

<span data-ttu-id="963c1-204">В следующем примере кода VBScript описывается подключение к удаленному компьютеру для получения данных [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) .</span><span class="sxs-lookup"><span data-stu-id="963c1-204">The following VBScript code example describes how to connect to a remote computer to obtain [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) data.</span></span> <span data-ttu-id="963c1-205">Имя домена, указанное в *стрдомаин* , используется в *страусорити*.</span><span class="sxs-lookup"><span data-stu-id="963c1-205">The domain name that is specified in *strDomain* is used in *strAuthority*.</span></span>


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



<span data-ttu-id="963c1-206">Следующий фрагмент кода PowerShell обращается к удаленному серверу и перечисляет доступные классы WMI.</span><span class="sxs-lookup"><span data-stu-id="963c1-206">The following PowerShell snippet access a remote server and lists the available WMI classes.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="963c1-207">Требования</span><span class="sxs-lookup"><span data-stu-id="963c1-207">Requirements</span></span>



| <span data-ttu-id="963c1-208">Требование</span><span class="sxs-lookup"><span data-stu-id="963c1-208">Requirement</span></span> | <span data-ttu-id="963c1-209">Значение</span><span class="sxs-lookup"><span data-stu-id="963c1-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="963c1-210">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="963c1-210">Minimum supported client</span></span><br/> | <span data-ttu-id="963c1-211">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="963c1-211">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="963c1-212">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="963c1-212">Minimum supported server</span></span><br/> | <span data-ttu-id="963c1-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="963c1-213">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="963c1-214">Header</span><span class="sxs-lookup"><span data-stu-id="963c1-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="963c1-215"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="963c1-215"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="963c1-216">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="963c1-216">Type library</span></span><br/>             | <dl> <span data-ttu-id="963c1-217"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="963c1-217"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="963c1-218">DLL</span><span class="sxs-lookup"><span data-stu-id="963c1-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963c1-219"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="963c1-219"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="963c1-220">CLSID</span><span class="sxs-lookup"><span data-stu-id="963c1-220">CLSID</span></span><br/>                    | <span data-ttu-id="963c1-221">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="963c1-221">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="963c1-222">IID</span><span class="sxs-lookup"><span data-stu-id="963c1-222">IID</span></span><br/>                      | <span data-ttu-id="963c1-223">IID \_ исвбемлокатор</span><span class="sxs-lookup"><span data-stu-id="963c1-223">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="963c1-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="963c1-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="963c1-225">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="963c1-225">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="963c1-226">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="963c1-226">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="963c1-227">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="963c1-227">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="963c1-228">Создание скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="963c1-228">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> </dl>

 

