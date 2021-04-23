---
title: Конфигурация подключаемого модуля службы WinRM
description: Подключаемый модуль служба удаленного управления Windows (WinRM) должен быть зарегистрирован в каталоге WinRM, чтобы инфраструктура динамически определила набор доступных подключаемых модулей и URI ресурсов, которые они поддерживают.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104339605"
---
# <a name="winrm-service-plug-in-configuration"></a><span data-ttu-id="553b1-103">Конфигурация подключаемого модуля службы WinRM</span><span class="sxs-lookup"><span data-stu-id="553b1-103">WinRM Service Plug-in Configuration</span></span>

<span data-ttu-id="553b1-104">Подключаемый модуль служба удаленного управления Windows (WinRM) должен быть зарегистрирован в каталоге WinRM, чтобы инфраструктура динамически определила набор доступных подключаемых модулей и [*URI ресурсов*](windows-remote-management-glossary.md) , которые они поддерживают.</span><span class="sxs-lookup"><span data-stu-id="553b1-104">A Windows Remote Management (WinRM) plug-in must be registered in the WinRM catalog to enable the infrastructure to dynamically determine the set of available plug-ins and the [*resource URIs*](windows-remote-management-glossary.md) that they support.</span></span> <span data-ttu-id="553b1-105">Все [*URI ресурсов*](windows-remote-management-glossary.md) для подключаемых модулей WinRM должны соответствовать формату, определенному в RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ).</span><span class="sxs-lookup"><span data-stu-id="553b1-105">All [*resource URIs*](windows-remote-management-glossary.md) for WinRM plug-ins should conform to the format that is defined in RFC 3986 ([https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt)).</span></span> <span data-ttu-id="553b1-106">Настройка выполняется с помощью основной службы WinRM.</span><span class="sxs-lookup"><span data-stu-id="553b1-106">Configuration is done through the main WinRM service.</span></span>

<span data-ttu-id="553b1-107">Следующая команда регистрирует конфигурацию подключаемого модуля в службе WinRM:</span><span class="sxs-lookup"><span data-stu-id="553b1-107">The following command registers a plug-in configuration with the WinRM service:</span></span>

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> <span data-ttu-id="553b1-108">Чтобы предоставить новые зарегистрированные подключаемые модули, необходимо перезапустить службу WinRM.</span><span class="sxs-lookup"><span data-stu-id="553b1-108">The WinRM service needs to be restarted to expose the newly registered plug-ins.</span></span>

<span data-ttu-id="553b1-109">Конфигурация подключаемого модуля указывается в формате XML.</span><span class="sxs-lookup"><span data-stu-id="553b1-109">Plug-in configuration is specified in XML.</span></span> <span data-ttu-id="553b1-110">Пример.</span><span class="sxs-lookup"><span data-stu-id="553b1-110">The following is an example.</span></span>

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



<span data-ttu-id="553b1-111">В следующем списке описаны XML-элементы более подробно и за ним следует схема конфигурации, указанная в виде XSD.</span><span class="sxs-lookup"><span data-stu-id="553b1-111">The following list describes the XML elements in more detail and is followed by the configuration schema specified as an XSD.</span></span>

<dl> <dt>

<span data-ttu-id="553b1-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**Плугинконфигуратион** / **Оператионсконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="553b1-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration**/**OperationsConfiguration**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-113">Указывает имя файла подключаемого модуля операций.</span><span class="sxs-lookup"><span data-stu-id="553b1-113">Specifies the file name of the operations plug-in.</span></span> <span data-ttu-id="553b1-114">Все переменные среды, помещаемые в эту запись, будут развернуты в контексте пользователя при последующем запросе.</span><span class="sxs-lookup"><span data-stu-id="553b1-114">Any environment variables that are put in this entry will be expanded in the users' context when a request comes in.</span></span> <span data-ttu-id="553b1-115">У каждого пользователя может быть другая версия одной и той же переменной среды, поэтому каждый пользователь может использовать другой подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="553b1-115">Each user could have a different version of the same environment variable, so each user could end up with a different plug-in.</span></span> <span data-ttu-id="553b1-116">Эта запись не может быть пустой и должна указывать на допустимый подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="553b1-116">This entry cannot be blank and must point to a valid plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**Плугинконфигуратион** / **Имя**</span><span class="sxs-lookup"><span data-stu-id="553b1-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration**/**Name**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-118">Указывает отображаемое имя, используемое для подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="553b1-118">Specifies the display name to use for the plug-in.</span></span> <span data-ttu-id="553b1-119">Если из подключаемого модуля возвращается ошибка, то это имя помещается в XML-код ошибки, который возвращается клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="553b1-119">If an error is returned from the plug-in, this name will be put into the error XML that is returned to the client application.</span></span> <span data-ttu-id="553b1-120">Это имя может быть на любом языке.</span><span class="sxs-lookup"><span data-stu-id="553b1-120">The name is not locale specific.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**Плугинконфигуратион** / **Архитектура**</span><span class="sxs-lookup"><span data-stu-id="553b1-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration**/**Architecture**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-122">Указывает, является ли подключаемый модуль операций 32-разрядным или 64-битным.</span><span class="sxs-lookup"><span data-stu-id="553b1-122">Specifies whether the operations plug-in is 32-bit or 64-bit.</span></span> <span data-ttu-id="553b1-123">Если этот элемент не указан, по умолчанию будет установлено значение "32" в системах x86, а в 64-разрядных системах — "64".</span><span class="sxs-lookup"><span data-stu-id="553b1-123">If this element is not specified, the value will default to "32" on x86 systems and to "64" on 64-bit systems.</span></span> <span data-ttu-id="553b1-124">Для систем x86 единственным допустимым значением является "32".</span><span class="sxs-lookup"><span data-stu-id="553b1-124">For x86 systems, the only valid value is "32".</span></span> <span data-ttu-id="553b1-125">Если значение равно "32" в 64-разрядной системе, при вводе сведений о **имени файла** необходимо учитывать перенаправление WOW64.</span><span class="sxs-lookup"><span data-stu-id="553b1-125">If the value is "32" on an 64-bit system, wow64 redirection needs to be taken into account when entering the **Filename** information.</span></span> <span data-ttu-id="553b1-126">Базовая файловая система будет использовать перенаправление WOW64 для преобразования system32 в syswow64.</span><span class="sxs-lookup"><span data-stu-id="553b1-126">The underlying file system will use wow64 redirection to translate system32 to syswow64.</span></span> <span data-ttu-id="553b1-127">Например, если **filename** имеет значение "% WINDIR% \\ system32 \\myplugin.dll" и **архитектура** — "32", фактический файл подключаемого модуля находится в папке "% WINDIR% \\ SysWOW64 \\myplugin.dll".</span><span class="sxs-lookup"><span data-stu-id="553b1-127">For example, if **Filename** is "%windir%\\system32\\myplugin.dll" and **Architecture** is "32", the actual plug-in file is located at "%windir%\\syswow64\\myplugin.dll".</span></span>

</dd> <dt>

<span data-ttu-id="553b1-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**Плугинконфигуратион** / **Ксмлрендерингтипе**</span><span class="sxs-lookup"><span data-stu-id="553b1-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration**/**XmlRenderingType**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-129">Настраивает формат, в котором XML передается в подключаемые модули через [**объект \_ данных WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) .</span><span class="sxs-lookup"><span data-stu-id="553b1-129">Configures the format in which XML is passed to plug-ins through the [**WSMAN\_DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) object.</span></span> <span data-ttu-id="553b1-130">Доступны следующие типы.</span><span class="sxs-lookup"><span data-stu-id="553b1-130">The following types are available:</span></span>

<dl> <dt>

<span data-ttu-id="553b1-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Полнотекстовым</span><span class="sxs-lookup"><span data-stu-id="553b1-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="553b1-132">Входящие XML-данные содержатся в \_ \_ \_ текстовой структуре WSMan типа данных, которая представляет XML как **пквстр** буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="553b1-132">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_TEXT structure, which represents the XML as a **PCWSTR** memory buffer.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>Чтения</span><span class="sxs-lookup"><span data-stu-id="553b1-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span></span>
</dt> <dd>

<span data-ttu-id="553b1-134">Входящие XML-данные содержатся в \_ \_ \_ \_ структуре модуля чтения XML типа данных WSMan WS \_ , которая представляет XML как объект **XmlReader** , который определен в файле заголовка WebService. h.</span><span class="sxs-lookup"><span data-stu-id="553b1-134">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_WS\_XML\_READER structure, which represents the XML as an **XmlReader** object, which is defined in the WebServices.h header file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="553b1-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**Плугинконфигуратион** / **Инитиализатионксмл**</span><span class="sxs-lookup"><span data-stu-id="553b1-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration**/**InitializationXml**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-136">Этот узел является необязательным и позволяет подключаемому модулю настроить дополнительный XML, который будет передан методу [**всманплугинстартуп**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).</span><span class="sxs-lookup"><span data-stu-id="553b1-136">This node is optional and allows a plug-in to configure extra XML that will be passed in to the [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)method.</span></span> <span data-ttu-id="553b1-137">Большинству подключаемых модулей эти дополнительные сведения не понадобятся, но если подключаемый модуль должен использоваться в нескольких сценариях, требующих другой семантики времени выполнения, этот XML предоставит подключаемому модулю такую гибкость.</span><span class="sxs-lookup"><span data-stu-id="553b1-137">Most plug-ins will not need this extra information, but if a plug-in needs to be used under more than one scenario that requires different run-time semantics, this XML will give the plug-in the flexibility to do this.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**Плугинконфигуратион** / **Ресурсы**</span><span class="sxs-lookup"><span data-stu-id="553b1-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration**/**Resources**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-139">Указывает список [*URI ресурсов*](windows-remote-management-glossary.md), поддерживаемых этим подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="553b1-139">Specifies a list of [*resource URIs*](windows-remote-management-glossary.md)that this plug-in supports.</span></span> <span data-ttu-id="553b1-140">Необходимо указать по меньшей мере одну запись **ResourceUri**; в противном случае XML будет отклонен.</span><span class="sxs-lookup"><span data-stu-id="553b1-140">At least one **ResourceUri** entry must be specified; otherwise, the XML will be rejected.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс**</span><span class="sxs-lookup"><span data-stu-id="553b1-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration**/**Resources**/**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-142">Представляет одну конфигурацию [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-142">Represents a single [*resource URI*](windows-remote-management-glossary.md)configuration.</span></span>

> [!Note]  
> <span data-ttu-id="553b1-143">Для атрибута **суппортсоптионс** можно задать значение false.</span><span class="sxs-lookup"><span data-stu-id="553b1-143">The **SupportsOptions** attribute can be set to false.</span></span> <span data-ttu-id="553b1-144">Если для **суппортсоптионс** задано значение false, этот атрибут не указывается при перечислении ресурса.</span><span class="sxs-lookup"><span data-stu-id="553b1-144">If **SupportsOptions** is set to false, this attribute is not listed when the resource is enumerated.</span></span>

 

</dd> <dt>

<span data-ttu-id="553b1-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс** / **ResourceUri**</span><span class="sxs-lookup"><span data-stu-id="553b1-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration**/**Resources**/**Resource**/**ResourceUri**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-146">Указывает один [*URI ресурса*](windows-remote-management-glossary.md) либо в полной, либо в виде частичной строки соответствия на основе атрибута **ExactMatch** .</span><span class="sxs-lookup"><span data-stu-id="553b1-146">Specifies a single [*resource URI*](windows-remote-management-glossary.md) either in full or as a partial match string based on the **ExactMatch** attribute.</span></span> <span data-ttu-id="553b1-147">Если **ExactMatch** отсутствует, по умолчанию используется **значение false**, означающее, что обработчик WinRM SOAP выполняет частичное сопоставление с началом *URI ресурса* , а при наличии совпадения передает его в подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="553b1-147">If **ExactMatch** is not present, it defaults to **False**, which means the WinRM SOAP processor will do a partial match to the start of the *resource URI* and, if there is a match, pass it to the plug-in.</span></span> <span data-ttu-id="553b1-148">Атрибут **суппортсоптионс** можно указать, если этому *URI ресурса* разрешено передавать любые параметры.</span><span class="sxs-lookup"><span data-stu-id="553b1-148">The **SupportsOptions** attribute can be specified if this *resource URI* is allowed to have any options passed in.</span></span> <span data-ttu-id="553b1-149">По умолчанию параметры не поддерживаются, и если они имеются в клиентском запросе, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="553b1-149">By default, no options are supported, and if any are present in the client request, an error will be returned.</span></span> <span data-ttu-id="553b1-150">Если параметры поддерживаются подключаемым модулем, то важно, чтобы подключаемый модуль возвращал правильную ошибку, если существует параметр, в котором подключаемый модуль не понимает, когда для флага **MustUnderstand** установлено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="553b1-150">If options are supported by the plug-in, it is important that the plug-in returns the correct error if an option is present that the plug-in does not understand when the **mustUnderstand** flag is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс** / **Возможности**</span><span class="sxs-lookup"><span data-stu-id="553b1-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Capability**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-152">Указывает возможность, доступную в этом [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-152">Specifies a capability that is available on this [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-153">Для каждого поддерживаемого типа операции будет существовать одна запись.</span><span class="sxs-lookup"><span data-stu-id="553b1-153">There will be one entry for each type of operation that it supports.</span></span> <span data-ttu-id="553b1-154">Доступны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="553b1-154">The following options are available:</span></span>

<dl> <dt>

<span data-ttu-id="553b1-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Получить</span><span class="sxs-lookup"><span data-stu-id="553b1-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Get</span></span>
</dt> <dd>

<span data-ttu-id="553b1-156">Операции Get поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-156">Get operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-157">Атрибут **суппортфрагмент** используется, если операция get поддерживает концепцию.</span><span class="sxs-lookup"><span data-stu-id="553b1-157">The **SupportFragment** attribute is used if the get operation supports the concept.</span></span> <span data-ttu-id="553b1-158">Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение false.</span><span class="sxs-lookup"><span data-stu-id="553b1-158">The **SupportFiltering** attribute is not valid and should be set to false.</span></span> <span data-ttu-id="553b1-159">Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="553b1-159">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>PUT</span><span class="sxs-lookup"><span data-stu-id="553b1-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Put</span></span>
</dt> <dd>

<span data-ttu-id="553b1-161">Операции размещения поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-161">Put operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-162">Атрибут **суппортфрагмент** используется, если операция размещения поддерживает концепцию.</span><span class="sxs-lookup"><span data-stu-id="553b1-162">The **SupportFragment** attribute is used if the put operation supports the concept.</span></span> <span data-ttu-id="553b1-163">Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-163">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="553b1-164">Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="553b1-164">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Создания</span><span class="sxs-lookup"><span data-stu-id="553b1-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Create</span></span>
</dt> <dd>

<span data-ttu-id="553b1-166">Операции создания поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-166">Create operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-167">Атрибут **суппортфрагмент** используется, если операция создания поддерживает концепцию.</span><span class="sxs-lookup"><span data-stu-id="553b1-167">The **SupportFragment** attribute is used if the create operation supports the concept.</span></span> <span data-ttu-id="553b1-168">Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-168">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="553b1-169">Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="553b1-169">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Удален</span><span class="sxs-lookup"><span data-stu-id="553b1-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Delete</span></span>
</dt> <dd>

<span data-ttu-id="553b1-171">Операции Delete поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-171">Delete operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-172">Атрибут **суппортфрагмент** используется, если операция удаления поддерживает концепцию.</span><span class="sxs-lookup"><span data-stu-id="553b1-172">The **SupportFragment** attribute is used if the delete operation supports the concept.</span></span> <span data-ttu-id="553b1-173">Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-173">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="553b1-174">Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="553b1-174">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Вызвать</span><span class="sxs-lookup"><span data-stu-id="553b1-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invoke</span></span>
</dt> <dd>

<span data-ttu-id="553b1-176">Операции Invoke поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-176">Invoke operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-177">Атрибут **суппортфрагмент** не поддерживается для операций Invoke и должен иметь значение false.</span><span class="sxs-lookup"><span data-stu-id="553b1-177">The **SupportFragment** attribute is not supported for invoke operations and should be set to false.</span></span> <span data-ttu-id="553b1-178">Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-178">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="553b1-179">Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="553b1-179">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Перечислить</span><span class="sxs-lookup"><span data-stu-id="553b1-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerate</span></span>
</dt> <dd>

<span data-ttu-id="553b1-181">Операции перечисления поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-181">Enumerate operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-182">Атрибут **суппортфрагмент** не поддерживается для операций перечисления и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-182">The **SupportFragment** attribute is not supported for enumerate operations and should be set to **False**.</span></span> <span data-ttu-id="553b1-183">Атрибут **суппортфилтеринг** является допустимым, и если подключаемый модуль поддерживает фильтрацию, для этого атрибута необходимо задать значение **true**.</span><span class="sxs-lookup"><span data-stu-id="553b1-183">The **SupportFiltering** attribute is valid, and if the plug-in supports filtering this attribute should be set to **True**.</span></span> <span data-ttu-id="553b1-184">Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="553b1-184">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Наблюдателя</span><span class="sxs-lookup"><span data-stu-id="553b1-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Subscribe</span></span>
</dt> <dd>

<span data-ttu-id="553b1-186">Операции подписки поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-186">Subscribe operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-187">Атрибут **суппортфрагмент** не поддерживается для операций подписки и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-187">The **SupportFragment** attribute is not supported for subscribe operations and should be set to **False**.</span></span> <span data-ttu-id="553b1-188">Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-188">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="553b1-189">Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="553b1-189">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="553b1-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Консоль</span><span class="sxs-lookup"><span data-stu-id="553b1-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span></span>
</dt> <dd>

<span data-ttu-id="553b1-191">Операции оболочки поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="553b1-191">Shell operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="553b1-192">Атрибут **суппортфрагмент** не поддерживается для операций оболочки и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-192">The **SupportFragment** attribute is not supported for shell operations and should be set to **False**.</span></span> <span data-ttu-id="553b1-193">Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="553b1-193">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="553b1-194">Эта возможность недопустима для *URI ресурса* , если также поддерживается любая другая операция.</span><span class="sxs-lookup"><span data-stu-id="553b1-194">This capability is not valid for a *resource URI* if any other operation capability is also supported.</span></span> <span data-ttu-id="553b1-195">Если для *универсального кода ресурса (URI)* настроена возможность работы с оболочкой, то операции получения, размещения, создания, удаления, вызова и перечисления обрабатываются внутри службы WinRM для управления оболочками.</span><span class="sxs-lookup"><span data-stu-id="553b1-195">If a shell operation capability is configured for a *resource URI*, then get, put, create, delete, invoke, and enumerate operations are processed internally within the WinRm service to manage shells.</span></span> <span data-ttu-id="553b1-196">В результате подключаемый модуль не может работать с самими операциями.</span><span class="sxs-lookup"><span data-stu-id="553b1-196">As a result, the plug-in cannot deal with the operations itself.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="553b1-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс** / **Безопасность**</span><span class="sxs-lookup"><span data-stu-id="553b1-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Security**</span></span>
</dt> <dd>

<span data-ttu-id="553b1-198">Этот элемент определяет дескриптор безопасности (через атрибут **SDDL** ), который должен применяться для определения доступа к определенному [*URI ресурса*](windows-remote-management-glossary.md) (через атрибут **URI** ).</span><span class="sxs-lookup"><span data-stu-id="553b1-198">This element defines the security descriptor (via the **Sddl** attribute) that should be applied to determine access to a particular [*resource URI*](windows-remote-management-glossary.md) (via the **Uri** attribute).</span></span> <span data-ttu-id="553b1-199">Если **ExactMatch** отсутствует, элемент **безопасности** по умолчанию имеет **значение false**, что означает, что **SDDL** применяется ко всем *URI ресурсов* , которые используют **универсальный код ресурса (URI)** в качестве префикса.</span><span class="sxs-lookup"><span data-stu-id="553b1-199">If **ExactMatch** is not present, the **Security** element defaults to **False**, which means that the **Sddl** applies to all *resource URIs* that share **Uri** as a prefix.</span></span> <span data-ttu-id="553b1-200">Если для **ExactMatch** задано значение true, то **SDDL** применяется только к указанному точному **URI** .</span><span class="sxs-lookup"><span data-stu-id="553b1-200">If **ExactMatch** is set to true, the **Sddl** applies only to the exact **Uri** specified.</span></span> <span data-ttu-id="553b1-201">При наличии нескольких записей **безопасности** , которые могут применяться к определенным *URI ресурса*, для определения соответствующего **SDDL** используется наиболее длинное совпадение префиксов.</span><span class="sxs-lookup"><span data-stu-id="553b1-201">If there are multiple **Security** entries that could apply to a particular *resource URIs*, the longest-prefix match is used to determine the appropriate **Sddl**.</span></span> <span data-ttu-id="553b1-202">В результате совпадения с наибольшим префиксом, если запись **URI** точного соответствия существует, она всегда будет выбрана в качестве соответствующего элемента безопасности.</span><span class="sxs-lookup"><span data-stu-id="553b1-202">As a result of the longest-prefix match, if an exact-match **Uri** entry exists, it will always be chosen as the appropriate Security element.</span></span>

</dd> </dl>

<span data-ttu-id="553b1-203">Ниже приведена схема конфигурации подключаемого модуля, заданная как XSD.</span><span class="sxs-lookup"><span data-stu-id="553b1-203">The following is the plug-in configuration schema specified as an XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




