---
description: По умолчанию приложение или скрипт получает данные от соответствующего поставщика, если существуют две версии поставщиков.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Запрос данных WMI на 64-разрядной платформе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692708"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="ba20f-103">Запрос данных WMI на 64-разрядной платформе</span><span class="sxs-lookup"><span data-stu-id="ba20f-103">Requesting WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="ba20f-104">По умолчанию приложение или скрипт получает данные от соответствующего поставщика, если существуют две версии поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ba20f-104">By default, an application or script receives data from the corresponding provider when two versions of providers exist.</span></span> <span data-ttu-id="ba20f-105">32-разрядный поставщик возвращает данные в 32-разрядное приложение, включая все сценарии, а 64-разрядный поставщик возвращает данные в 64-разрядные скомпилированные приложения.</span><span class="sxs-lookup"><span data-stu-id="ba20f-105">The 32-bit provider returns data to a 32-bit application, including all scripts, and the 64-bit provider returns data to the 64-bit compiled applications.</span></span> <span data-ttu-id="ba20f-106">Однако приложение или скрипт может запрашивать данные от поставщика, не используемого по умолчанию, если он существует, уведомляя WMI с помощью флагов в вызовах методов.</span><span class="sxs-lookup"><span data-stu-id="ba20f-106">However, an application or script can request data from the nondefault provider, if it exists, by notifying WMI through flags on method calls.</span></span>

## <a name="context-flags"></a><span data-ttu-id="ba20f-107">Флаги контекста</span><span class="sxs-lookup"><span data-stu-id="ba20f-107">Context Flags</span></span>

<span data-ttu-id="ba20f-108">Строковые флаги **\_ \_ провидерарчитектуре** и **\_ \_ рекуиредарчитектуре** имеют набор значений, обрабатываемых WMI, но не определенные в файлах заголовка пакета SDK или библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="ba20f-108">The **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** string flags have a set of values handled by WMI but not defined in SDK header or type library files.</span></span> <span data-ttu-id="ba20f-109">Значения помещаются в параметр контекста для сигнализации инструментария WMI о том, что он должен запрашивать данные от поставщика, не используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba20f-109">The values are placed in a context parameter to signal WMI that it should request data from the nondefault provider.</span></span>

<span data-ttu-id="ba20f-110">Ниже перечислены флаги и их возможные значения.</span><span class="sxs-lookup"><span data-stu-id="ba20f-110">The following lists the flags and their possible values.</span></span>

<dl> <dt>

<span data-ttu-id="ba20f-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_провидерарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="ba20f-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="ba20f-112">Целочисленное значение 32 или 64, которое указывает 32-разрядную или 64-разрядную версию.</span><span class="sxs-lookup"><span data-stu-id="ba20f-112">Integer value, either 32 or 64, that specifies the 32-bit or 64-bit version.</span></span>

</dd> <dt>

<span data-ttu-id="ba20f-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_рекуиредарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="ba20f-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="ba20f-114">Логическое значение, используемое в дополнение к **\_ \_ провидерарчитектуре** для принудительной загрузки указанной версии поставщика.</span><span class="sxs-lookup"><span data-stu-id="ba20f-114">Boolean value used in addition to **\_\_ProviderArchitecture** to force load the specified provider version.</span></span> <span data-ttu-id="ba20f-115">Если версия недоступна, WMI возвращает ошибку 0x80041013, **вбемеррпровидерлоадфаилуре** для Visual Basic и **\_ \_ \_ \_ сбой загрузки поставщика WBEM E** для C++.</span><span class="sxs-lookup"><span data-stu-id="ba20f-115">If the version is unavailable, then WMI returns the error 0x80041013, **wbemErrProviderLoadFailure** for Visual Basic and **WBEM\_E\_PROVIDER\_LOAD\_FAILURE** for C++.</span></span> <span data-ttu-id="ba20f-116">Значение по умолчанию для этого флага, если оно не указано, равно **false**.</span><span class="sxs-lookup"><span data-stu-id="ba20f-116">The default value for this flag when it is not specified is **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="ba20f-117">В 64-разрядной системе, которая имеет параллельные версии поставщика, 32-разрядное приложение или скрипт автоматически получает данные от поставщика 32-bit, если эти флаги не указаны и не указывают на то, что должны быть возвращены данные, посвященные 64-разрядному поставщику.</span><span class="sxs-lookup"><span data-stu-id="ba20f-117">On a 64-bit system that has side-by-side versions of a provider, a 32-bit application or script automatically receives data from the 32-bit provider, unless these flags are supplied and indicate that the 64-bit provider data should be returned.</span></span>

## <a name="using-the-context-flags"></a><span data-ttu-id="ba20f-118">Использование флагов контекста</span><span class="sxs-lookup"><span data-stu-id="ba20f-118">Using the Context Flags</span></span>

<span data-ttu-id="ba20f-119">Приложения C++ могут использовать интерфейс [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) с [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) для обмена данными с использованием поставщика, не используемого по умолчанию, с WMI.</span><span class="sxs-lookup"><span data-stu-id="ba20f-119">C++ applications can use the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface with [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to communicate the use of a nondefault provider to WMI.</span></span>

<span data-ttu-id="ba20f-120">В скриптах и Visual Basic необходимо создать объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , содержащий флаги для параметра *Обжвбемнамедвалуесет* в [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="ba20f-120">In scripting and Visual Basic, you must create a [**SWbemNamedValueSet**](swbemnamedvalueset.md) object containing the flags for the *objWbemNamedValueSet* parameter of [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="ba20f-121">Дополнительные сведения о настройке объектов параметров для этого вызова см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ba20f-121">For more information about setting up the parameters objects for this call, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="ba20f-122">Вы можете безопасно запускать сценарии и приложения с помощью контекстных флагов в более старых операционных системах, так как инструментарий WMI игнорирует их в системах, где они не реализованы.</span><span class="sxs-lookup"><span data-stu-id="ba20f-122">You can safely run scripts and applications using the context flags in older operating systems, because WMI ignores them in systems in which they are not implemented.</span></span> <span data-ttu-id="ba20f-123">Хотя существует 32-разрядная и 64-разрядная версии поставщика системного реестра, обратите внимание, что существует только одна версия репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="ba20f-123">While 32-bit and 64-bit versions of the System Registry provider exist, note that only one version of the WMI repository exists.</span></span>

## <a name="accessing-the-default-registry-hive"></a><span data-ttu-id="ba20f-124">Доступ к кусту реестра по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba20f-124">Accessing the Default Registry Hive</span></span>

<span data-ttu-id="ba20f-125">В приведенной ниже серии примеров используется [поставщик реестра](/previous-versions/windows/desktop/regprov/system-registry-provider), который имеет параллельную 32-разрядную и 64-разрядные версии, предварительно установленные в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="ba20f-125">The following series of examples use the [Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which has side-by-side 32-bit and 64-bit versions preinstalled on 64-bit operating systems.</span></span> <span data-ttu-id="ba20f-126">В этих примерах 32-разрядные клиенты получают данные, возвращенные поставщиком из 32-разрядного **узла \_ hKey \_ \\ Software \\ WOW6432Node \\ Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="ba20f-126">In these examples, 32-bit clients get data returned by the provider from the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft**.</span></span> <span data-ttu-id="ba20f-127">64-разрядные клиенты получают данные, возвращаемые поставщиком, из 64-разрядного узла **hKey \_ локальный \_ компьютер \\ программное обеспечение \\ \\ ведение журнала Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="ba20f-127">64-bit clients get data returned by the provider from the 64-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Logging**.</span></span>

<span data-ttu-id="ba20f-128">В сценариях показано, как вызывать методы класса [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) в реестре с помощью [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md) для получения данных из 32-разрядного куста реестра.</span><span class="sxs-lookup"><span data-stu-id="ba20f-128">The scripts show how to call the methods of the Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class through [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to obtain data from the 32-bit registry hive.</span></span>

<span data-ttu-id="ba20f-129">Следующий скрипт получает данные от поставщика, которые соответствуют битовой ширине вызывающего объекта (в данном случае 64 бит), так как это сценарий, выполняющийся в 64-разрядном сервере сценариев Windows (WSH).</span><span class="sxs-lookup"><span data-stu-id="ba20f-129">The following script gets back data from the provider that matches the bit width of the caller, in this case 64 bits, because it is a script running under the 64-bit Windows Script Host (WSH).</span></span> <span data-ttu-id="ba20f-130">Сценарий получает значение из 64-разрядного узла реестра **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM \\ ведение журнала** , а не 32-разрядный узел **hKey \_ Local \_ Machine \\ Software \\ WOW6432Node \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="ba20f-130">The script gets the value from the 64-bit registry node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM\\Logging** rather than the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\WBEM\\CIMOM**.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



<span data-ttu-id="ba20f-131">Если значение параметра **Logging** в кусте по умолчанию равно 1, то выходные данные скрипта должны выглядеть примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ba20f-131">If the **Logging** value in the default hive is set to 1, then the output from the script should look something like the following:</span></span>

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="ba20f-132">Пример. в частности, запрашивается 32-разрядный куст реестра на 64-разрядном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ba20f-132">Example: Specifically Requesting the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="ba20f-133">В следующем измененном примере сценария по умолчанию используется флаг строки **\_ \_ провидерарчитектуре** для запроса доступа к 32-разрядным данным реестра на 64-разрядном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ba20f-133">The following modified example of the default script uses the **\_\_ProviderArchitecture** string flag to request access to the 32-bit registry data on a 64-bit computer.</span></span> <span data-ttu-id="ba20f-134">Вызывающий объект подключается к 32-разрядному Hive независимо от того, является ли это приложение 32 или 64-bit.</span><span class="sxs-lookup"><span data-stu-id="ba20f-134">The caller is connected to the 32-bit hive irrespective of whether it is a 32- or 64-bit application.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="ba20f-135">Пример. принудительное применение WMI для доступа к кусту реестра 32-bit на 64-разрядном компьютере</span><span class="sxs-lookup"><span data-stu-id="ba20f-135">Example: Forcing WMI to Access the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="ba20f-136">Следующее изменение сценария выше путем добавления флагов **\_ \_ провидерарчитектуре** и **\_ \_ рекуиредарчитектуре** в параметр context заставляет Инструментарий WMI загрузить 32-разрядный поставщик и получить 32-разрядные данные.</span><span class="sxs-lookup"><span data-stu-id="ba20f-136">The following modification of the script above by adding the **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** flags to the context parameter forces WMI to load the 32-bit provider and get 32-bit data.</span></span> <span data-ttu-id="ba20f-137">Если поставщик не существует, возникает ошибка загрузки поставщика.</span><span class="sxs-lookup"><span data-stu-id="ba20f-137">If the provider does not exist, then a provider load error occurs.</span></span> <span data-ttu-id="ba20f-138">Объект контекста должен быть предоставлен в соединении с WMI путем вызова [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="ba20f-138">The context object must be supplied in the connection to WMI by calling [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a><span data-ttu-id="ba20f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="ba20f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba20f-140">Получение и предоставление данных на 64-разрядном компьютере</span><span class="sxs-lookup"><span data-stu-id="ba20f-140">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
