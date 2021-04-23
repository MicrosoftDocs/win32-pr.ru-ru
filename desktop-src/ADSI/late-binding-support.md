---
title: Поддержка поздних привязок
description: Если установлена поддержка позднего связывания, каждый вызов функции должен пройти через интерфейс ADSI IDispatch, прежде чем перенаправлять его в соответствующее расширение.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- расширения ADSI, поддержка поздних привязок
- ADSI ADSI, пример кода Visual Basic, поддержка позднего связывания
- Привязка AD, поддержка позднего связывания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793884"
---
# <a name="late-binding-support"></a><span data-ttu-id="70427-106">Поддержка поздних привязок</span><span class="sxs-lookup"><span data-stu-id="70427-106">Late Binding Support</span></span>

<span data-ttu-id="70427-107">Если установлена поддержка позднего связывания, каждый вызов функции должен пройти через интерфейс ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , прежде чем перенаправлять его в соответствующее расширение.</span><span class="sxs-lookup"><span data-stu-id="70427-107">When late binding support is in place, each function call must go through the ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface, before it is rerouted to the appropriate extension.</span></span>

<span data-ttu-id="70427-108">Рассмотрим следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="70427-108">Consider the following code example.</span></span>


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



<span data-ttu-id="70427-109">Нет явных вызовов метода **QueryInterface** для получения расширений.</span><span class="sxs-lookup"><span data-stu-id="70427-109">There are no explicit calls to the **QueryInterface** method to get to the extensions.</span></span> <span data-ttu-id="70427-110">Расширения должны перенаправлять свои вызовы [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в интерфейс ADSI **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="70427-110">The extensions must reroute their [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) calls to the ADSI **IDispatch** interface.</span></span> <span data-ttu-id="70427-111">ADSI принимает решение и разрешает любые возникающие конфликты, а затем перенаправляет обратно в соответствующее расширение с помощью интерфейса с именем [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="70427-111">ADSI makes the decision and resolves any conflicts that occur, then it re-routes back to the appropriate extension using an interface called [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span> <span data-ttu-id="70427-112">Таким образом, любое расширение, которое поддерживает позднее связывание, должно реализовывать **иадсекстенсион**.</span><span class="sxs-lookup"><span data-stu-id="70427-112">Therefore, any extension that supports late binding must implement **IADsExtension**.</span></span>

 

 