---
description: По умолчанию приложение или скрипт получает данные от соответствующего поставщика, если существуют две версии поставщиков.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Запрос данных WMI на 64-разрядной платформе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320aaec9f11600e3b963a01fe9dcddbd6c4f1f3fd98df8ff2311417ddcd6fef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995784"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>Запрос данных WMI на 64-разрядной платформе

По умолчанию приложение или скрипт получает данные от соответствующего поставщика, если существуют две версии поставщиков. 32-разрядный поставщик возвращает данные в 32-разрядное приложение, включая все сценарии, а 64-разрядный поставщик возвращает данные в 64-разрядные скомпилированные приложения. Однако приложение или скрипт может запрашивать данные от поставщика, не используемого по умолчанию, если он существует, уведомляя WMI с помощью флагов в вызовах методов.

## <a name="context-flags"></a>Флаги контекста

Строковые флаги **\_ \_ провидерарчитектуре** и **\_ \_ рекуиредарчитектуре** имеют набор значений, обрабатываемых WMI, но не определенные в файлах заголовка пакета SDK или библиотеки типов. Значения помещаются в параметр контекста для сигнализации инструментария WMI о том, что он должен запрашивать данные от поставщика, не используемого по умолчанию.

Ниже перечислены флаги и их возможные значения.

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_провидерарчитектуре**
</dt> <dd>

Целочисленное значение 32 или 64, которое указывает 32-разрядную или 64-разрядную версию.

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_рекуиредарчитектуре**
</dt> <dd>

Логическое значение, используемое в дополнение к **\_ \_ провидерарчитектуре** для принудительной загрузки указанной версии поставщика. если версия недоступна, WMI возвращает ошибку 0x80041013, **вбемеррпровидерлоадфаилуре** для Visual Basic и **\_ \_ \_ \_ сбой загрузки поставщика WBEM E** для C++. Значение по умолчанию для этого флага, если оно не указано, равно **false**.

</dd> </dl>

В 64-разрядной системе, которая имеет параллельные версии поставщика, 32-разрядное приложение или скрипт автоматически получает данные от поставщика 32-bit, если эти флаги не указаны и не указывают на то, что должны быть возвращены данные, посвященные 64-разрядному поставщику.

## <a name="using-the-context-flags"></a>Использование флагов контекста

Приложения C++ могут использовать интерфейс [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) с [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) для обмена данными с использованием поставщика, не используемого по умолчанию, с WMI.

в скриптах и Visual Basic необходимо создать объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , содержащий флаги для параметра *обжвбемнамедвалуесет* в [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md). Дополнительные сведения о настройке объектов параметров для этого вызова см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

Вы можете безопасно запускать сценарии и приложения с помощью контекстных флагов в более старых операционных системах, так как инструментарий WMI игнорирует их в системах, где они не реализованы. Хотя существует 32-разрядная и 64-разрядная версии поставщика системного реестра, обратите внимание, что существует только одна версия репозитория WMI.

## <a name="accessing-the-default-registry-hive"></a>Доступ к кусту реестра по умолчанию

В приведенной ниже серии примеров используется [поставщик реестра](/previous-versions/windows/desktop/regprov/system-registry-provider), который имеет параллельную 32-разрядную и 64-разрядные версии, предварительно установленные в 64-разрядных операционных системах. В этих примерах 32-разрядные клиенты получают данные, возвращенные поставщиком из 32-разрядного **узла \_ hKey \_ \\ Software \\ WOW6432Node \\ Майкрософт**. 64-разрядные клиенты получают данные, возвращаемые поставщиком, из 64-разрядного узла **hKey \_ локальный \_ компьютер \\ программное обеспечение \\ \\ ведение журнала Майкрософт**.

В сценариях показано, как вызывать методы класса [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) в реестре с помощью [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md) для получения данных из 32-разрядного куста реестра.

следующий скрипт получает данные от поставщика, которые соответствуют битовой ширине вызывающего объекта (в данном случае 64 бит), так как это сценарий, выполняющийся в 64-разрядном Windows сервере сценариев (WSH). Сценарий получает значение из 64-разрядного узла реестра **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM \\ ведение журнала** , а не 32-разрядный узел **hKey \_ Local \_ Machine \\ Software \\ WOW6432Node \\ Microsoft \\ WBEM \\ CIMOM**.


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



Если значение параметра **Logging** в кусте по умолчанию равно 1, то выходные данные скрипта должны выглядеть примерно следующим образом:

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Пример. в частности, запрашивается 32-разрядный куст реестра на 64-разрядном компьютере.

В следующем измененном примере сценария по умолчанию используется флаг строки **\_ \_ провидерарчитектуре** для запроса доступа к 32-разрядным данным реестра на 64-разрядном компьютере. Вызывающий объект подключается к 32-разрядному Hive независимо от того, является ли это приложение 32 или 64-bit.


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



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Пример. принудительное применение WMI для доступа к кусту реестра 32-bit на 64-разрядном компьютере

Следующее изменение сценария выше путем добавления флагов **\_ \_ провидерарчитектуре** и **\_ \_ рекуиредарчитектуре** в параметр context заставляет Инструментарий WMI загрузить 32-разрядный поставщик и получить 32-разрядные данные. Если поставщик не существует, возникает ошибка загрузки поставщика. Объект контекста должен быть предоставлен в соединении с WMI путем вызова [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md).


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Получение и предоставление данных на 64-разрядном компьютере](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
