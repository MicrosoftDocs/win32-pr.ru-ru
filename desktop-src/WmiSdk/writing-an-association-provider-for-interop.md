---
description: Поставщик взаимосвязей предоставляет механизм для регистрации профилей и связывания их с профилями, реализованными в разных пространствах имен.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Написание поставщика ассоциаций для взаимодействия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105714065"
---
# <a name="writing-an-association-provider-for-interop"></a><span data-ttu-id="77897-103">Написание поставщика ассоциаций для взаимодействия</span><span class="sxs-lookup"><span data-stu-id="77897-103">Writing an Association Provider for Interop</span></span>

<span data-ttu-id="77897-104">Поставщик взаимосвязей предоставляет механизм для регистрации профилей и связывания их с профилями, реализованными в разных пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="77897-104">An association provider provides a mechanism to register profiles and associate them with profiles that are implemented in different namespaces.</span></span>

<span data-ttu-id="77897-105">Поставщики ассоциаций используются для предоставления стандартных профилей, таких как профиль питания.</span><span class="sxs-lookup"><span data-stu-id="77897-105">Association providers are used to expose standard profiles, like a power profile.</span></span> <span data-ttu-id="77897-106">Это достигается путем записи поставщика ассоциаций в корневое пространство имен/Interop, которое предоставляет экземпляры ассоциаций путем реализации класса, производного от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77897-106">This is accomplished by writing an association provider in the root/interop namespace that exposes association instances by implementing a class, which is derived from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span> <span data-ttu-id="77897-107">Для поддержки обхода перекрестного пространства имен поставщик должен быть зарегистрирован как в корневом, так и в ходе, а также в корневом/ <implemented> пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="77897-107">The provider must be registered in both the root/interop and the root/<implemented> namespace to support cross namespace traversal.</span></span>

<span data-ttu-id="77897-108">Инструментарий управления Windows (WMI) (WMI) загружает поставщик ассоциаций каждый раз, когда запрос ассоциации выполняется в пространстве имен root или Interop.</span><span class="sxs-lookup"><span data-stu-id="77897-108">Windows Management Instrumentation (WMI) loads the association provider whenever an association query is run in the root/interop namespace.</span></span>

<span data-ttu-id="77897-109">**Реализация поставщика взаимосвязей для взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="77897-109">**To implement an association provider for interop**</span></span>

1.  <span data-ttu-id="77897-110">Производные классы от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) и создают статический экземпляр этого производного класса в корневом \\ пространстве имен взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="77897-110">Derive a class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and create a static instance of this derived class in the root\\interop namespace.</span></span> <span data-ttu-id="77897-111">Как минимум, следующие свойства должны распространяться на допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="77897-111">At a minimum, the following properties must be propagated with valid values:</span></span>

    -   <span data-ttu-id="77897-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77897-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="77897-113">[**регистереднаме**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77897-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="77897-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77897-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="77897-115">[**регистередверсион**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77897-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span></span>

    <span data-ttu-id="77897-116">Хотя [**InstanceId**](/previous-versions//ee309375(v=vs.85)) уникально определяет экземпляр **\_ Регистередпрофиле CIM**, сочетание **регистереднаме**, **RegisteredOrganization** и **регистередверсион** должно однозначно идентифицировать зарегистрированный профиль в области организации.</span><span class="sxs-lookup"><span data-stu-id="77897-116">Even though [**InstanceID**](/previous-versions//ee309375(v=vs.85)) uniquely defines the instance of the **CIM\_RegisteredProfile**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="77897-117">Дополнительные сведения об отдельных свойствах см. в разделе [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77897-117">For more information about the individual properties, see [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

    <span data-ttu-id="77897-118">В следующем примере кода описывается синтаксис для наследования класса **процесспрофиле** от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) и заполнения статического экземпляра.</span><span class="sxs-lookup"><span data-stu-id="77897-118">The following code example describes the syntax for deriving the **ProcessProfile** class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and populating the static instance.</span></span>

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > <span data-ttu-id="77897-119">Для клиентов Windows свойству **RegisteredOrganization** должно быть присвоено значение 1, а свойству **Осеррегистередорганизатион** — значение Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77897-119">For Windows clients, the **RegisteredOrganization** property must be set to 1 and the **OtherRegisteredOrganization** property set to "Microsoft".</span></span>

     

2.  <span data-ttu-id="77897-120">Создайте поставщик, возвращающий экземпляры ассоциаций [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span><span class="sxs-lookup"><span data-stu-id="77897-120">Create a provider that returns association instances of [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span></span> <span data-ttu-id="77897-121">Этот процесс состоит из двух шагов.</span><span class="sxs-lookup"><span data-stu-id="77897-121">This is a two-step process.</span></span>

    1.  <span data-ttu-id="77897-122">Создайте класс, производный от [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в пространствах имен взаимодействия и реализации.</span><span class="sxs-lookup"><span data-stu-id="77897-122">Create a class that is derived from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in both the interop and implementation namespaces.</span></span> <span data-ttu-id="77897-123">Поскольку один и тот же профиль может быть реализован разными поставщиками, имя класса должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="77897-123">Because the same profile can be implemented by different vendors, the name of the class should be unique.</span></span> <span data-ttu-id="77897-124">Рекомендуемое соглашение об именовании — " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ".</span><span class="sxs-lookup"><span data-stu-id="77897-124">The recommended naming convention is "<Organization>\_<ProductName>\_<ClassName>\_<Version>".</span></span> <span data-ttu-id="77897-125">Свойство **конформантстандард** или **манажеделемент** должно указывать квалификатор **MSFT \_ targetNamespace** , содержащий пространство имен, к которому принадлежит этот класс.</span><span class="sxs-lookup"><span data-stu-id="77897-125">Either the **ConformantStandard** or the **ManagedElement** property must specify the **MSFT\_TargetNamespace** qualifier that contains the namespace to which this class belongs.</span></span>

        <span data-ttu-id="77897-126">В следующем примере кода описывается синтаксис для наследования \_ класса Microsoft Process \_ елементконформстопрофиле \_ v1 от [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в корневом \\ пространстве имен Interop.</span><span class="sxs-lookup"><span data-stu-id="77897-126">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\interop namespace.</span></span> <span data-ttu-id="77897-127">В этом примере \_ управляемый элемент процесса Win32 ссылается на корневое \\ пространство имен CIMV2 с помощью квалификатора **MSFT \_ targetNamespace** .</span><span class="sxs-lookup"><span data-stu-id="77897-127">In this example, the Win32\_Process managed element references the root\\cimv2 namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="77897-128">В следующем примере кода описывается синтаксис для наследования \_ класса Microsoft Process \_ елементконформстопрофиле \_ v1 от [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="77897-128">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="77897-129">В этом примере согласованный стандарт [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) ссылается на корневое \\ пространство имен взаимодействия с помощью квалификатора **MSFT \_ targetNamespace** .</span><span class="sxs-lookup"><span data-stu-id="77897-129">In this example, the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conformant standard references the root\\interop namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="77897-130">Если квалификатор **MSFT \_ targetNamespace** не задан для свойства, ссылающегося на реализованное пространство имен, фильтр **ресулткласс** оператора "соединители" не будет работать.</span><span class="sxs-lookup"><span data-stu-id="77897-130">If the **MSFT\_TargetNamespace** qualifier is not specified on the property that is referencing the implemented namespace, the **ResultClass** filter of "Associators of" statement will not work.</span></span> <span data-ttu-id="77897-131">Например, если квалификатор **MSFT \_ targetNamespace** не указан, следующая командная строка Windows PowerShell не будет возвращать объект: **Get-WmiObject-Query "-соединители {процесспрофиле. InstanceId = ' Process '}, где Ресулткласс =" \_ процесс Win32 "**.</span><span class="sxs-lookup"><span data-stu-id="77897-131">For example, if the **MSFT\_TargetNamespace** qualifier is not specified, the following Windows PowerShell command-line will not return an object: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32\_Process'"**.</span></span>

        <span data-ttu-id="77897-132">Квалификатор **MSFT \_ targetNamespace** не может указывать на пространство имен на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="77897-132">The **MSFT\_TargetNamespace** qualifier cannot point to a namespace on a remote computer.</span></span> <span data-ttu-id="77897-133">Например, следующее пространство имен не поддерживается: MSFT \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ корневое \\ \\ взаимодействие).</span><span class="sxs-lookup"><span data-stu-id="77897-133">For example, the following namespace is not supported: MSFT\_TargetNamespace(\\\\\\\\<RemoteMachine>\\\\root\\\\interop).</span></span>

    2.  <span data-ttu-id="77897-134">Напишите поставщик, возвращающий экземпляры созданного производного класса.</span><span class="sxs-lookup"><span data-stu-id="77897-134">Write a provider that returns instances of the created derived class.</span></span> <span data-ttu-id="77897-135">Дополнительные сведения см. в разделе [написание поставщика экземпляров](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="77897-135">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span> <span data-ttu-id="77897-136">При доступе к экземплярам перекрестного пространства имен может потребоваться доступ к уровням безопасности клиента.</span><span class="sxs-lookup"><span data-stu-id="77897-136">When you access cross-namespace instances, you might have to access the security levels for the client.</span></span> <span data-ttu-id="77897-137">Дополнительные сведения см. в разделе [олицетворение клиента](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="77897-137">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

        <span data-ttu-id="77897-138">Поставщик взаимосвязей должен реализовывать методы [**IWbemServices. креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) и [**IWbemServices. жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="77897-138">The association provider should implement both the [**IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) and [**IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span> <span data-ttu-id="77897-139">Реализовать метод [**IWbemServices.Exeккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) необязательно.</span><span class="sxs-lookup"><span data-stu-id="77897-139">Implementing the [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method is optional.</span></span> <span data-ttu-id="77897-140">Поскольку доступ к этому поставщику можно получить как из корневого взаимодействия, так \\ и из корневых \\ <implemented> пространств имен, не должно быть явной зависимости от пространства имен внутри поставщика.</span><span class="sxs-lookup"><span data-stu-id="77897-140">Because this provider can be accessed from both the root\\interop and the root\\<implemented> namespaces, there should not be an explicit dependency on a namespace inside the provider.</span></span>

3.  <span data-ttu-id="77897-141">Зарегистрируйте поставщика ассоциаций как в корневом, так \\ и в корневом \\ <implemented> пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="77897-141">Register the association provider in both the root\\interop and the root\\<implemented> namespaces.</span></span> <span data-ttu-id="77897-142">Дополнительные сведения см. в разделе [Регистрация поставщика экземпляров](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="77897-142">For more information, see [Registering an Instance Provider](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="77897-143">В следующем примере кода описывается синтаксис для регистрации поставщика ассоциаций в корневом \\ пространстве имен взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="77897-143">The following code example describes the syntax to register the association provider in the root\\interop namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    <span data-ttu-id="77897-144">В следующем примере кода описан синтаксис для регистрации поставщика взаимосвязей в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="77897-144">The following code example describes the syntax to register the association provider in the root\\cimv2 namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  <span data-ttu-id="77897-145">Поместите схему для [**\_ елементконформстопрофиле CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в реализованное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="77897-145">Place the schema for the [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) into the implemented namespace.</span></span> <span data-ttu-id="77897-146">Для клиентов Windows это файл Interop. mof, расположенный в папке% systemroot% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="77897-146">For Windows clients this is the interop.mof file that is located in the %systemroot%\\system32\\wbem folder.</span></span>
5.  <span data-ttu-id="77897-147">Реализуйте интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="77897-147">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="77897-148">Инструментарий WMI использует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для загрузки и инициализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="77897-148">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="77897-149">Метод [**IWbemProviderInit.Iniтиализе**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) должен быть реализован таким образом, который позволяет вызывать его для двух разных пространств имен.</span><span class="sxs-lookup"><span data-stu-id="77897-149">The [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method should be implemented in a way that allows it to be called for two different namespaces.</span></span> <span data-ttu-id="77897-150">Дополнительные сведения см. [в разделе Инициализация поставщика](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="77897-150">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77897-151">См. также</span><span class="sxs-lookup"><span data-stu-id="77897-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77897-152">**\_ЕЛЕМЕНТКОНФОРМСТОПРОФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="77897-152">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

<span data-ttu-id="77897-153">[**\_РЕГИСТЕРЕДПРОФИЛЕ CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77897-153">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="77897-154">Написание поставщика экземпляров</span><span class="sxs-lookup"><span data-stu-id="77897-154">Writing an Instance Provider</span></span>](writing-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="77897-155">Регистрация поставщика экземпляра</span><span class="sxs-lookup"><span data-stu-id="77897-155">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

 
