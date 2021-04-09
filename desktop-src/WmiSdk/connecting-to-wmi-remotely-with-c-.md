---
description: Как и в случае с другими языками, такими как PowerShell, VBScript или C++, можно использовать C# для удаленного мониторинга оборудования и программного обеспечения на удаленных компьютерах.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Удаленное подключение к инструментарию WMI с помощью C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ad9fe2008b52276a8f68149b33ae3729daaf7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081211"
---
# <a name="connecting-to-wmi-remotely-with-c"></a><span data-ttu-id="2cad3-103">Удаленное подключение к инструментарию WMI с помощью C #</span><span class="sxs-lookup"><span data-stu-id="2cad3-103">Connecting to WMI Remotely with C#</span></span>

<span data-ttu-id="2cad3-104">Как и в случае с другими языками, такими как PowerShell, VBScript или C++, можно использовать C# для удаленного мониторинга оборудования и программного обеспечения на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="2cad3-104">As with other languages such as PowerShell, VBScript, or C++, you can use C# to remotely monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="2cad3-105">Удаленные соединения для управляемого кода выполняются с помощью пространства имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2cad3-105">Remote connections for managed code are accomplished through the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace.</span></span> <span data-ttu-id="2cad3-106">(В предыдущих версиях WMI использовалось пространство имен [System. Management](/dotnet/api/system.management) , которое включено для полноты.)</span><span class="sxs-lookup"><span data-stu-id="2cad3-106">(Previous versions of WMI used the [System.Management](/dotnet/api/system.management) namespace, which is included here for completeness.)</span></span>

> [!Note]  
> <span data-ttu-id="2cad3-107">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="2cad3-107">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="2cad3-108">Удаленное подключение с помощью классов в пространстве имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) использует DCOM в качестве базового удаленного механизма.</span><span class="sxs-lookup"><span data-stu-id="2cad3-108">Connecting remotely using classes in the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace uses DCOM as the underlying remote mechanism.</span></span> <span data-ttu-id="2cad3-109">Удаленные подключения WMI должны соответствовать требованиям безопасности DCOM в отношении проверки подлинности и олицетворения.</span><span class="sxs-lookup"><span data-stu-id="2cad3-109">WMI remote connections must comply with DCOM security requirements for impersonation and authentication.</span></span> <span data-ttu-id="2cad3-110">По умолчанию область привязана к локальному компьютеру и \\ пространству имен "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="2cad3-110">By default, a scope is bound to the local computer and the "Root\\CIMv2" system namespace.</span></span> <span data-ttu-id="2cad3-111">Однако можно изменить доступное пространство имен компьютера, домена и инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="2cad3-111">However, you can change both the computer, domain, and WMI namespace that you access.</span></span> <span data-ttu-id="2cad3-112">Вы также можете задать параметры полномочий, олицетворения, учетных данных и других параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="2cad3-112">You can also set authority, impersonation, credentials, and other connection options.</span></span>

<span data-ttu-id="2cad3-113">**Удаленное подключение к инструментарию WMI с помощью C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="2cad3-113">**To connect to WMI remotely with C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="2cad3-114">Создайте сеанс на удаленном компьютере, вызвав [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cad3-114">Create a session on the remote machine with a call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span></span>

    <span data-ttu-id="2cad3-115">При подключении к удаленному компьютеру с использованием тех же учетных данных (домен и имя пользователя), которые вошли в систему, можно указать имя компьютера в вызове [CREATE](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2cad3-115">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the name of the computer in the [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) call.</span></span> <span data-ttu-id="2cad3-116">После получения возвращенного объекта [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) можно выполнить запрос WMI.</span><span class="sxs-lookup"><span data-stu-id="2cad3-116">Once you have the returned [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object, you can then make your WMI query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    <span data-ttu-id="2cad3-117">Дополнительные сведения о выполнении запросов WMI с помощью API **Microsoft. Management. Infrastructure** в C# см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="2cad3-117">For more information on making WMI queries with the **Microsoft.Management.Infrastructure** API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="2cad3-118">Если вы хотите задать различные параметры для подключения, такие как другие учетные данные, языковой стандарт или уровень олицетворения, необходимо использовать объект [Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) в вызове [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cad3-118">If you wish to set different options for your connection, such as different credentials, locale or Impersonation levels, you need to use a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) object in your call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span></span>

    <span data-ttu-id="2cad3-119">[Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) является базовым классом для [всмансессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) и [дкомсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cad3-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) is a base class for [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) and [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span></span> <span data-ttu-id="2cad3-120">Можно использовать для настройки параметров в сеансах WS-Man и DCOM соответственно.</span><span class="sxs-lookup"><span data-stu-id="2cad3-120">You can use either to set the options on your WS-Man and DCOM sessions, respectively.</span></span> <span data-ttu-id="2cad3-121">В следующем образце кода описывается использование объекта [дкомсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) для задания уровня олицетворения для олицетворения.</span><span class="sxs-lookup"><span data-stu-id="2cad3-121">The following code sample describes using a [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) object to set the Impersonation level to Impersonate.</span></span>

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  <span data-ttu-id="2cad3-122">Если вы хотите задать учетные данные для подключения, необходимо создать и добавить объект [Цимкредентиалс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) в [Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cad3-122">If you wish to set the credentials for your connection, you will need to create and add a [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) object to your [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span></span>

    <span data-ttu-id="2cad3-123">В следующем примере кода описывается создание класса [всмансессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , его заполнение соответствующим [Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))и его использование в вызове [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2cad3-123">The following code sample describes creating a [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) class, filling it with the proper [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)), and using it in a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) call.</span></span>

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    <span data-ttu-id="2cad3-124">Обычно не рекомендуется жестко кодировать пароль в приложениях. как показано в приведенном выше примере кода, по возможности попытайтесь запросить пароль у пользователя и безопасно сохранить его.</span><span class="sxs-lookup"><span data-stu-id="2cad3-124">It is generally recommended that you do not hardcode a password into your applications; as the above code sample indicates, whenever possible try to query your user for the password, and store it securely.</span></span>

<span data-ttu-id="2cad3-125">Инструментарий WMI предназначен для наблюдения за аппаратным и программным обеспечением на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="2cad3-125">WMI is intended to monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="2cad3-126">Удаленные соединения для WMI v1 выполняются через объект [манажементскопе](/dotnet/api/system.management.managementscope) .</span><span class="sxs-lookup"><span data-stu-id="2cad3-126">Remote connections for WMI v1 is accomplished through the [ManagementScope](/dotnet/api/system.management.managementscope) object.</span></span>

<span data-ttu-id="2cad3-127">**Удаленное подключение к инструментарию WMI с помощью C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="2cad3-127">**To connect to WMI remotely with C# (System.Management)**</span></span>

1.  <span data-ttu-id="2cad3-128">Создайте объект [манажементскопе](/dotnet/api/system.management.managementscope) , используя имя компьютера и путь WMI, и подключитесь к целевому объекту с помощью вызова Манажементскопе. Connect ().</span><span class="sxs-lookup"><span data-stu-id="2cad3-128">Create a [ManagementScope](/dotnet/api/system.management.managementscope) object, using the name of the computer and the WMI path, and connect to your target with a call to ManagementScope.Connect().</span></span>

    <span data-ttu-id="2cad3-129">Если вы подключаетесь к удаленному компьютеру с использованием тех же учетных данных (домен и имя пользователя), которые вошли в систему, необходимо указать только путь WMI.</span><span class="sxs-lookup"><span data-stu-id="2cad3-129">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you only have to specify the WMI path.</span></span> <span data-ttu-id="2cad3-130">После подключения можно сделать запрос WMI.</span><span class="sxs-lookup"><span data-stu-id="2cad3-130">Once you have connected, you can make your WMI query.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    <span data-ttu-id="2cad3-131">Дополнительные сведения о выполнении запросов WMI с помощью API [System. Management](/dotnet/api/system.management) в C# см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="2cad3-131">For more information on making WMI queries with the [System.Management](/dotnet/api/system.management) API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="2cad3-132">Если вы подключаетесь к удаленному компьютеру в другом домене или используете другое имя пользователя и пароль, необходимо использовать объект [ConnectionOptions](/dotnet/api/system.management.connectionoptions) в вызове [манажементскопе](/dotnet/api/system.management.managementscope).</span><span class="sxs-lookup"><span data-stu-id="2cad3-132">If you connect to a remote computer in a different domain or using a different user name and password, then you must use a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) object in the call to the [ManagementScope](/dotnet/api/system.management.managementscope).</span></span>

    <span data-ttu-id="2cad3-133">[ConnectionOptions](/dotnet/api/system.management.connectionoptions) содержит свойства для описания проверки подлинности, олицетворения, имени пользователя, пароля и других параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="2cad3-133">The [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contains properties for describing the Authentication, Impersonation, username, password, and other connection options.</span></span> <span data-ttu-id="2cad3-134">В следующем образце кода описывается использование [ConnectionOptions](/dotnet/api/system.management.connectionoptions) для установки уровня олицетворения для олицетворения.</span><span class="sxs-lookup"><span data-stu-id="2cad3-134">The following code sample describes using a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) to set the Impersonation Level to Impersonate.</span></span>

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    <span data-ttu-id="2cad3-135">В общем случае рекомендуется задать для уровня олицетворения олицетворение, если в противном случае не требуется явно.</span><span class="sxs-lookup"><span data-stu-id="2cad3-135">Generally speaking, it is recommended that you set your Impersonation level to Impersonate unless explicitly needed otherwise.</span></span> <span data-ttu-id="2cad3-136">Кроме того, старайтесь не писать свое имя и пароль в коде C#.</span><span class="sxs-lookup"><span data-stu-id="2cad3-136">Further, try to avoid writing your name and password into C# code.</span></span> <span data-ttu-id="2cad3-137">(Если это возможно, см. Дополнительные сведения о том, можно ли отправить запрос пользователю на динамическое предоставление во время выполнения.)</span><span class="sxs-lookup"><span data-stu-id="2cad3-137">(If possible, see if you can query the user to dynamically supply them at runtime.)</span></span>

    <span data-ttu-id="2cad3-138">Дополнительные примеры настройки различных свойств для удаленного подключения WMI см. в разделе "примеры" на странице справочника по [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="2cad3-138">For more examples of setting different properties on a remote WMI connection, see the Examples section of the [ConnectionOptions](/dotnet/api/system.management.connectionoptions) reference page.</span></span>

## <a name="microsoftmanagementinfrastructure-example"></a><span data-ttu-id="2cad3-139">Пример Microsoft. Management. Infrastructure</span><span class="sxs-lookup"><span data-stu-id="2cad3-139">Microsoft.Management.Infrastructure Example</span></span>

<span data-ttu-id="2cad3-140">Следующий пример кода C#, основанный на следующей [записи блога на TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), описывает, как использовать [Цимкредентиалс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) и [всмансессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) для установки учетных данных на удаленном подключении.</span><span class="sxs-lookup"><span data-stu-id="2cad3-140">The following C# code example, based on the following [blog post on TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), describes how to use [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) and [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) to set credentials on a remote connection.</span></span>


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a><span data-ttu-id="2cad3-141">Пример System. Management</span><span class="sxs-lookup"><span data-stu-id="2cad3-141">System.Management Example</span></span>

<span data-ttu-id="2cad3-142">В следующем образце кода C# описывается общее удаленное подключение с помощью объектов System. Management.</span><span class="sxs-lookup"><span data-stu-id="2cad3-142">The following C# code sample describes a general remote connection, using the System.Management objects.</span></span>


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="2cad3-143">См. также</span><span class="sxs-lookup"><span data-stu-id="2cad3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cad3-144">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="2cad3-144">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
