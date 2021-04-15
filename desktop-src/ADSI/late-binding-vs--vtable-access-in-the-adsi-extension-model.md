---
title: Позднее связывание и доступ к vtable в модели расширения ADSI
description: Сдвоенный интерфейс обеспечивает прямой доступ к всем функциям vtable при отсутствии интерфейса диспетчеризации.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- позднее связывание и доступ к vtable в модели расширения ADSI
- расширения ADSI, позднее связывание и доступ vtable в модели расширения ADSI
- ADSI ADSI, пример кода Visual Basic, использование Иадсдуалинф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654368"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a><span data-ttu-id="9301d-106">Позднее связывание и доступ к vtable в модели расширения ADSI</span><span class="sxs-lookup"><span data-stu-id="9301d-106">Late Binding vs. Vtable Access in the ADSI Extension Model</span></span>

<span data-ttu-id="9301d-107">Сдвоенный интерфейс обеспечивает прямой доступ к всем функциям vtable при отсутствии интерфейса диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="9301d-107">A dual interface enables direct vtable access to all its functions while a dispatch interface does not.</span></span> <span data-ttu-id="9301d-108">Клиент C/C++ может запросить указатель сдвоенного интерфейса и использовать прямой доступ к таблице vtable для вызова своих функций.</span><span class="sxs-lookup"><span data-stu-id="9301d-108">A C/C++ client can query for a dual interface pointer and use direct vtable access to invoke its functions.</span></span> <span data-ttu-id="9301d-109">Это обеспечивает более быстрый доступ, чем вызов функции с помощью функций [**IDispatch:: GetIdsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) и [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="9301d-109">This provides faster access than invoking the function using the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions.</span></span> <span data-ttu-id="9301d-110">Это особенно справедливо в модели расширения, так как все сдвоенные интерфейсы в объекте расширения должны сначала делегировать свои **GetIDsOfNames** и **вызывать** функции в агрегатор (ADSI).</span><span class="sxs-lookup"><span data-stu-id="9301d-110">This is especially true in the extension model, because all dual interfaces in an extension object must delegate their **GetIDsOfNames** and **Invoke** functions back to the aggregator (ADSI) first.</span></span> <span data-ttu-id="9301d-111">Затем агрегатор должен выполнить дополнительные внутренние шаги, чтобы выяснить, какой объект расширения, возможно, включая сам агрегатор, предоставляет поддержку функции, которая называется, и перенаправить вызов к соответствующему объекту.</span><span class="sxs-lookup"><span data-stu-id="9301d-111">The aggregator then must perform extra internal steps to identify which extension object, possibly including the aggregator itself, provides support for the function called and redirect the call to the appropriate object.</span></span>

<span data-ttu-id="9301d-112">Visual Basic также вызывает функцию с двумя интерфейсами, используя прямой доступ к таблице vtable, если у нее есть указатель на интерфейс и доступ к данным типа из библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="9301d-112">Visual Basic also invokes a dual-interface function using direct access to a vtable, if it has a pointer to the interface and access to type data from the type library.</span></span> <span data-ttu-id="9301d-113">Клиенты ADSI, написанные на Visual Basic, могут указать указатель на сдвоенный интерфейс, например [**iAds**](/windows/desktop/api/Iads/nn-iads-iads), явно, и таким образом разрешить доступ vtable к функциям в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9301d-113">ADSI clients written in Visual Basic can specify a pointer to a dual interface, for example, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitly, and thus enable vtable access to functions in the interface.</span></span>


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



<span data-ttu-id="9301d-114">Так как интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) не поддерживает доступ vtable, этот пример не применяется.</span><span class="sxs-lookup"><span data-stu-id="9301d-114">Because an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface does not support vtable access, this example does not apply.</span></span> <span data-ttu-id="9301d-115">Это значит, что функция диспетчеризации всегда вызывается только с помощью функций [**IDispatch:: GetIdsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) и [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="9301d-115">That is, a dispatch function is always invoked through the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions only.</span></span>

<span data-ttu-id="9301d-116">Текущие выпуски VBScript и JScript также не поддерживают доступ к vtable.</span><span class="sxs-lookup"><span data-stu-id="9301d-116">Current releases of VBScript and JScript also do not support vtable access.</span></span> <span data-ttu-id="9301d-117">Таким образом, сдвоенный интерфейс в среде VBScript или JScript работает как интерфейс диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="9301d-117">Therefore, a dual interface in a VBScript or JScript environment performs like a dispatch interface.</span></span>

 

 