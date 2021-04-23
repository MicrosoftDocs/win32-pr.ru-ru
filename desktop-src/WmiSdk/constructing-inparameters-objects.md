---
description: Объект параметров содержит список параметров для вызова методов поставщика при использовании типа вызова ExecMethod.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Построение объектов с параметрами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898802"
---
# <a name="constructing-inparameters-objects"></a><span data-ttu-id="5faba-103">Построение объектов с параметрами</span><span class="sxs-lookup"><span data-stu-id="5faba-103">Constructing InParameters Objects</span></span>

<span data-ttu-id="5faba-104">Объект [**параметров**](swbemmethod-inparameters.md) содержит список параметров для вызова методов поставщика при использовании типа вызова **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="5faba-104">An [**InParameters**](swbemmethod-inparameters.md) object contains the parameter list for calling provider methods when using an **ExecMethod** type of call.</span></span> <span data-ttu-id="5faba-105">Для [**всех методов \_SWbemObject.Exeкмесод**](swbemobject-execmethod-.md), [**SWbemObject.Exeкмесодасинк \_**](swbemobject-execmethodasync-.md), [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md)и [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md) требуется объект с **параметрами** .</span><span class="sxs-lookup"><span data-stu-id="5faba-105">The [**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods all require an **InParameters** object.</span></span>

<span data-ttu-id="5faba-106">Следующая процедура описывает, как создать объект с [**параметрами**](swbemmethod-inparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="5faba-106">The following procedure describes how to construct an [**InParameters**](swbemmethod-inparameters.md) object.</span></span>

<span data-ttu-id="5faba-107">**Создание параметра *обжвбеминпарамс***</span><span class="sxs-lookup"><span data-stu-id="5faba-107">**To construct the *objwbemInParams* parameter**</span></span>

1.  <span data-ttu-id="5faba-108">Подключитесь к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="5faba-108">Connect to WMI.</span></span>
2.  <span data-ttu-id="5faba-109">Получите определение класса WMI, определяющего метод, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="5faba-109">Obtain the definition of the WMI class that defines the method you want to execute.</span></span>
3.  <span data-ttu-id="5faba-110">Получите объект с [**параметрами**](swbemmethod-inparameters.md) , относящийся к методу класса WMI, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="5faba-110">Obtain an [**InParameters**](swbemmethod-inparameters.md) object specific to the WMI class method you want to execute.</span></span>

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  <span data-ttu-id="5faba-111">Задайте для свойств экземпляра значение, соответствующее значениям.</span><span class="sxs-lookup"><span data-stu-id="5faba-111">Set the properties of the instance to whatever values are appropriate.</span></span> <span data-ttu-id="5faba-112">Обязательно присвойте значения ключевым свойствам в классе WMI, содержащем метод, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="5faba-112">Be sure to give values to the key properties in the WMI class that contains the method you want to execute.</span></span>

    <span data-ttu-id="5faba-113">Например, если вы хотите задать входной параметр с именем минпутпарам в качестве значения "ABC" в экземпляре [**параметров**](swbemmethod-inparameters.md) , именуемых "inst", код будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5faba-113">For example, if you want to set an input parameter named myinputparam to the value "abc" in an instance of [**InParameters**](swbemmethod-inparameters.md) called "INST", the code would look like this.</span></span>

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  <span data-ttu-id="5faba-114">Выполните метод и получите возвращаемое состояние выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="5faba-114">Execute the method and obtain the return status of the method you are executing.</span></span>

<span data-ttu-id="5faba-115">В следующем примере кода показана настройка объекта [**параметров**](swbemmethod-inparameters.md) для создания нового объекта WMI, представляющего общую папку.</span><span class="sxs-lookup"><span data-stu-id="5faba-115">The following code example illustrates setting up the [**InParameters**](swbemmethod-inparameters.md) object to create a new WMI object that represents a share.</span></span> <span data-ttu-id="5faba-116">Дополнительные сведения об объекте [**Parameters**](swbemmethod-outparameters.md) см. в разделе [анализ объектов параметров](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5faba-116">For more information about the [**OutParameters**](swbemmethod-outparameters.md) object, see [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="5faba-117">Этот пример возвращает успешно возвращенное значение (0), если имеется папка с именем "Share" в расположении "C:/Share".</span><span class="sxs-lookup"><span data-stu-id="5faba-117">This example returns a successful return value (0) if there is a folder named "Share" at the location "C:/Share".</span></span> <span data-ttu-id="5faba-118">Этот пример позволяет предоставлять общий доступ к этой папке другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="5faba-118">This example enables this folder to be shared with other users.</span></span>


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



