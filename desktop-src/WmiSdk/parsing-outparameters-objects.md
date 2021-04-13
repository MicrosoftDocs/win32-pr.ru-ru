---
description: Объект Свбеммесод. parameters создается и предоставляется с данными с помощью метода поставщика, который исполняется.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Синтаксический анализ объектов параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348895"
---
# <a name="parsing-outparameters-objects"></a><span data-ttu-id="691b2-103">Синтаксический анализ объектов параметров</span><span class="sxs-lookup"><span data-stu-id="691b2-103">Parsing OutParameters Objects</span></span>

<span data-ttu-id="691b2-104">Объект [**свбеммесод. parameters**](swbemmethod-outparameters.md) создается и предоставляется с данными с помощью метода поставщика, который исполняется.</span><span class="sxs-lookup"><span data-stu-id="691b2-104">A [**SWbemMethod.OutParameters**](swbemmethod-outparameters.md) object is created and supplied with data by the provider method that is executing.</span></span> <span data-ttu-id="691b2-105">Свойства объекта **Parameters** относятся к методу, который называется.</span><span class="sxs-lookup"><span data-stu-id="691b2-105">Properties of the **OutParameters** object are specific to the method called.</span></span> <span data-ttu-id="691b2-106">Например, в приведенном ниже скрипте *SD* (содержащийся в *параметре*) является выходным параметром, определенным для метода **\_ \_ системсекурити. Возвращает** .</span><span class="sxs-lookup"><span data-stu-id="691b2-106">For example, in the script below, *SD* (contained in *outParam*) is the output parameter defined for the **\_\_SystemSecurity.GetSD** method.</span></span> <span data-ttu-id="691b2-107">Свойство **ReturnValue** является универсальным свойством, доступным для всех объектов **параметров** , которые содержат результат операции.</span><span class="sxs-lookup"><span data-stu-id="691b2-107">The **ReturnValue** property is a generic property available for all **OutParameters** objects which contain the result of the operation.</span></span>

<span data-ttu-id="691b2-108">В следующем примере кода показано получение выходных параметров из выполнения полученного [**метода в**](--systemsecurity-getsd.md) классе [**\_ \_ системсекурити**](--systemsecurity.md) для локальной системы.</span><span class="sxs-lookup"><span data-stu-id="691b2-108">The following code example illustrates obtaining output parameters from executing the [**GetSD**](--systemsecurity-getsd.md) method in class [**\_\_SystemSecurity**](--systemsecurity.md) for the local system.</span></span>


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



<span data-ttu-id="691b2-109">Дополнительные сведения см. в разделе [**свбеммесод. parameters**](swbemmethod-inparameters.md).</span><span class="sxs-lookup"><span data-stu-id="691b2-109">For more information, see [**SWbemMethod.InParameters**](swbemmethod-inparameters.md).</span></span>

 

 



