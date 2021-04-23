---
title: Поддержка раннего связывания
description: В следующем примере кода представлен сценарий с поддержкой раннего связывания на месте.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- расширения ADSI, поддержка раннего связывания
- Привязка AD, поддержка раннего связывания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134574"
---
# <a name="early-binding-support"></a><span data-ttu-id="77c8d-105">Поддержка раннего связывания</span><span class="sxs-lookup"><span data-stu-id="77c8d-105">Early Binding Support</span></span>

<span data-ttu-id="77c8d-106">В следующем примере кода представлен сценарий с поддержкой раннего связывания на месте.</span><span class="sxs-lookup"><span data-stu-id="77c8d-106">The following code example presents a scenario with early binding support in place.</span></span>


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



<span data-ttu-id="77c8d-107">В этом примере кода два компонента расширения расширяют объект **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="77c8d-107">In this code example, two extension components extend a **user** object.</span></span> <span data-ttu-id="77c8d-108">Каждое расширение публикует свой собственный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="77c8d-108">Each extension publishes its own interface.</span></span> <span data-ttu-id="77c8d-109">Каждое расширение не распознает другой интерфейс расширения; только интерфейсы ADSI распознают существование обоих расширений.</span><span class="sxs-lookup"><span data-stu-id="77c8d-109">Each extension does not recognize the other extension interface; only ADSI recognizes the existence of both extensions.</span></span> <span data-ttu-id="77c8d-110">Каждое расширение делегирует свой [**IUnknown интерфейсу**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ADSI.</span><span class="sxs-lookup"><span data-stu-id="77c8d-110">Each extension delegates its [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to ADSI.</span></span> <span data-ttu-id="77c8d-111">ADSI выступает в качестве агрегатора для обоих расширений и любых других расширений будущего.</span><span class="sxs-lookup"><span data-stu-id="77c8d-111">ADSI acts as an aggregator for both extensions, and any other future extensions.</span></span> <span data-ttu-id="77c8d-112">Запрос интерфейса из любого расширения или из ADSI дает одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="77c8d-112">Querying an interface from any extension, or from ADSI, yields the same consistent result.</span></span>

<span data-ttu-id="77c8d-113">В следующей процедуре описывается создание расширения.</span><span class="sxs-lookup"><span data-stu-id="77c8d-113">The following procedure describes how to create an extension.</span></span>

## <a name="step-1-add-aggregation-to-your-component"></a><span data-ttu-id="77c8d-114">Шаг 1. Добавление агрегата в компонент</span><span class="sxs-lookup"><span data-stu-id="77c8d-114">Step 1: Add Aggregation to Your Component</span></span>

<span data-ttu-id="77c8d-115">Следуйте спецификации COM, чтобы добавить статистическую функцию в компонент.</span><span class="sxs-lookup"><span data-stu-id="77c8d-115">Follow the COM specification for adding aggregation to your component.</span></span> <span data-ttu-id="77c8d-116">В заключение необходимо принять запросы *pUnknown* к компоненту во время выполнения **CreateInstance** и делегировать *pUnknown* в [**IUnknown-интерфейс**](/windows/win32/api/unknwn/nn-unknwn-iunknown) агрегатора, если компонент является агрегатным.</span><span class="sxs-lookup"><span data-stu-id="77c8d-116">In summary, you must accept the *pUnknown* requests to your component during **CreateInstance**, and delegate the *pUnknown* to the aggregator's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) if the component is aggregated.</span></span>

## <a name="step-2-register-your-extension"></a><span data-ttu-id="77c8d-117">Шаг 2. Регистрация расширения</span><span class="sxs-lookup"><span data-stu-id="77c8d-117">Step 2: Register Your Extension</span></span>

<span data-ttu-id="77c8d-118">Теперь необходимо выбрать класс каталога для расширения.</span><span class="sxs-lookup"><span data-stu-id="77c8d-118">Now you must decide which directory class to extend.</span></span> <span data-ttu-id="77c8d-119">Для этого нельзя использовать одни и те же интерфейсы, которые будут использоваться для интерфейса ADSI, например [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**иадскомпутер**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="77c8d-119">You cannot use the same interfaces to accomplish this that you would use for an ADSI interface, for example, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span></span> <span data-ttu-id="77c8d-120">Объекты каталога сохраняются в каталоге, в то время как расширение и ADSI выполняются на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="77c8d-120">Directory objects are persisted in the directory, while your extension and ADSI are running on the client computer.</span></span> <span data-ttu-id="77c8d-121">Примерами объектов каталога являются **User**, **Computer**, **очередь печати**, **serviceConnectionPoint** и **нтдссервице**.</span><span class="sxs-lookup"><span data-stu-id="77c8d-121">Directory object examples are **user**, **computer**, **printQueue**, **serviceConnectionPoint**, and **nTDSService**.</span></span> <span data-ttu-id="77c8d-122">Вы можете добавить новый класс в Active Directory и создать новое расширение для этого нового класса.</span><span class="sxs-lookup"><span data-stu-id="77c8d-122">You can add a new class in Active Directory and create a new extension for this new class as well.</span></span>

<span data-ttu-id="77c8d-123">С помощью разделов реестра можно связать имя класса каталога с компонентами расширения ADSI.</span><span class="sxs-lookup"><span data-stu-id="77c8d-123">You use registry keys to associate a directory class name with the ADSI extension components.</span></span> <span data-ttu-id="77c8d-124">На следующем рисунке представлена существующая структура реестра, а также новые ключи.</span><span class="sxs-lookup"><span data-stu-id="77c8d-124">The following figure represents the existing registry layout, as a well as new keys.</span></span>

-   <span data-ttu-id="77c8d-125">Новый ключ, именуемый **Extensions**, содержит список ключей, каждый из которых представляет класс в каталоге.</span><span class="sxs-lookup"><span data-stu-id="77c8d-125">A new key, called **Extensions**, contains a list of keys, each of which represents a class in the directory.</span></span> <span data-ttu-id="77c8d-126">Каждый класс, например **пользователь**, **очередь печати** или **компьютер**, хранит список подразделов.</span><span class="sxs-lookup"><span data-stu-id="77c8d-126">Each class, for example, **user**, **printQueue**, or **computer**, maintains a list of subkeys.</span></span>
-   <span data-ttu-id="77c8d-127">Каждый подраздел содержит идентификатор CLSID компонента расширения ADSI.</span><span class="sxs-lookup"><span data-stu-id="77c8d-127">Each subkey contains the CLSID of the ADSI extension component.</span></span>
-   <span data-ttu-id="77c8d-128">Каждый подраздел CLSID содержит запись строки, которая допускает несколько значений.</span><span class="sxs-lookup"><span data-stu-id="77c8d-128">Each CLSID subkey contains a string entry that allows multiple values.</span></span> <span data-ttu-id="77c8d-129">Необходимо только перечислить интерфейсы, участвующие в статистической обработке.</span><span class="sxs-lookup"><span data-stu-id="77c8d-129">You should only list the interfaces that participate in the aggregation.</span></span>

> [!Note]  
> <span data-ttu-id="77c8d-130">Объекты расширения по-прежнему необходимы для регистрации стандартных ключей COM.</span><span class="sxs-lookup"><span data-stu-id="77c8d-130">Extension objects are still required to register standard COM keys.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a><span data-ttu-id="77c8d-131">Пример</span><span class="sxs-lookup"><span data-stu-id="77c8d-131">Example</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

<span data-ttu-id="77c8d-132">Список интерфейсов из Extension1 может отличаться от "Extension2".</span><span class="sxs-lookup"><span data-stu-id="77c8d-132">The list of interfaces from Extension1 can be different from that of Extension2.</span></span> <span data-ttu-id="77c8d-133">Объект, если он активен, поддерживает интерфейсы агрегатора (ADSI) и все интерфейсы, предоставляемые Extension1 и Extension2 агрегата.</span><span class="sxs-lookup"><span data-stu-id="77c8d-133">The object, when active, supports the interfaces of the aggregator (ADSI) and all the interfaces provided by the aggregate's Extension1 and Extension2.</span></span> <span data-ttu-id="77c8d-134">Разрешение конфликтующих интерфейсов (тот же интерфейс, который поддерживается как агрегатором, так и агрегатами или несколькими агрегатами) определяется приоритетами расширений.</span><span class="sxs-lookup"><span data-stu-id="77c8d-134">Resolution of conflicting interfaces (the same interface supported by both the aggregator and the aggregates or by multiple aggregates) is determined by priorities of the extensions.</span></span>

<span data-ttu-id="77c8d-135">Вы также можете связать расширение CLSID с несколькими именами классов объектов.</span><span class="sxs-lookup"><span data-stu-id="77c8d-135">You can also associate your CLSID extension with multiple object class names.</span></span> <span data-ttu-id="77c8d-136">Например, расширение может расширять как объекты **пользователя** , так и **Контакты** .</span><span class="sxs-lookup"><span data-stu-id="77c8d-136">For example, your extension can extend both the **user** and **contact** objects.</span></span>

> [!Note]  
> <span data-ttu-id="77c8d-137">Поведение расширения добавляется в класс каждого объекта, а не на экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="77c8d-137">Extension behavior is added on a per-object class, not on a per-object instance.</span></span>

 

<span data-ttu-id="77c8d-138">Рекомендуется зарегистрировать расширения, как и любые другие компоненты COM, с помощью вызова функции **дллрегистерсвр** .</span><span class="sxs-lookup"><span data-stu-id="77c8d-138">As a best practice, register your extensions, as you would any other COM components, with a call to the **DllRegisterSvr** function.</span></span> <span data-ttu-id="77c8d-139">Кроме того, предоставьте возможность отмены регистрации расширения с помощью функции **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="77c8d-139">Also provide a facility to unregister your extension with the **DllUnregisterServer** function.</span></span>

<span data-ttu-id="77c8d-140">В следующем примере кода показано, как зарегистрировать расширение.</span><span class="sxs-lookup"><span data-stu-id="77c8d-140">The following code example shows how to register an extension.</span></span>


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 