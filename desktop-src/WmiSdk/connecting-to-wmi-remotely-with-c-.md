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
# <a name="connecting-to-wmi-remotely-with-c"></a>Удаленное подключение к инструментарию WMI с помощью C #

Как и в случае с другими языками, такими как PowerShell, VBScript или C++, можно использовать C# для удаленного мониторинга оборудования и программного обеспечения на удаленных компьютерах. Удаленные соединения для управляемого кода выполняются с помощью пространства имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) . (В предыдущих версиях WMI использовалось пространство имен [System. Management](/dotnet/api/system.management) , которое включено для полноты.)

> [!Note]  
> **System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .

 

Удаленное подключение с помощью классов в пространстве имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) использует DCOM в качестве базового удаленного механизма. Удаленные подключения WMI должны соответствовать требованиям безопасности DCOM в отношении проверки подлинности и олицетворения. По умолчанию область привязана к локальному компьютеру и \\ пространству имен "root CIMv2". Однако можно изменить доступное пространство имен компьютера, домена и инструментария WMI. Вы также можете задать параметры полномочий, олицетворения, учетных данных и других параметров соединения.

**Удаленное подключение к инструментарию WMI с помощью C# (Microsoft. Management. Infrastructure)**

1.  Создайте сеанс на удаленном компьютере, вызвав [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).

    При подключении к удаленному компьютеру с использованием тех же учетных данных (домен и имя пользователя), которые вошли в систему, можно указать имя компьютера в вызове [CREATE](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) . После получения возвращенного объекта [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) можно выполнить запрос WMI.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    Дополнительные сведения о выполнении запросов WMI с помощью API **Microsoft. Management. Infrastructure** в C# см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).

2.  Если вы хотите задать различные параметры для подключения, такие как другие учетные данные, языковой стандарт или уровень олицетворения, необходимо использовать объект [Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) в вызове [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).

    [Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) является базовым классом для [всмансессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) и [дкомсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)). Можно использовать для настройки параметров в сеансах WS-Man и DCOM соответственно. В следующем образце кода описывается использование объекта [дкомсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) для задания уровня олицетворения для олицетворения.

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  Если вы хотите задать учетные данные для подключения, необходимо создать и добавить объект [Цимкредентиалс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) в [Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).

    В следующем примере кода описывается создание класса [всмансессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , его заполнение соответствующим [Цимсессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))и его использование в вызове [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .

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

    

    Обычно не рекомендуется жестко кодировать пароль в приложениях. как показано в приведенном выше примере кода, по возможности попытайтесь запросить пароль у пользователя и безопасно сохранить его.

Инструментарий WMI предназначен для наблюдения за аппаратным и программным обеспечением на удаленных компьютерах. Удаленные соединения для WMI v1 выполняются через объект [манажементскопе](/dotnet/api/system.management.managementscope) .

**Удаленное подключение к инструментарию WMI с помощью C# (System. Management)**

1.  Создайте объект [манажементскопе](/dotnet/api/system.management.managementscope) , используя имя компьютера и путь WMI, и подключитесь к целевому объекту с помощью вызова Манажементскопе. Connect ().

    Если вы подключаетесь к удаленному компьютеру с использованием тех же учетных данных (домен и имя пользователя), которые вошли в систему, необходимо указать только путь WMI. После подключения можно сделать запрос WMI.

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    Дополнительные сведения о выполнении запросов WMI с помощью API [System. Management](/dotnet/api/system.management) в C# см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).

2.  Если вы подключаетесь к удаленному компьютеру в другом домене или используете другое имя пользователя и пароль, необходимо использовать объект [ConnectionOptions](/dotnet/api/system.management.connectionoptions) в вызове [манажементскопе](/dotnet/api/system.management.managementscope).

    [ConnectionOptions](/dotnet/api/system.management.connectionoptions) содержит свойства для описания проверки подлинности, олицетворения, имени пользователя, пароля и других параметров соединения. В следующем образце кода описывается использование [ConnectionOptions](/dotnet/api/system.management.connectionoptions) для установки уровня олицетворения для олицетворения.

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    В общем случае рекомендуется задать для уровня олицетворения олицетворение, если в противном случае не требуется явно. Кроме того, старайтесь не писать свое имя и пароль в коде C#. (Если это возможно, см. Дополнительные сведения о том, можно ли отправить запрос пользователю на динамическое предоставление во время выполнения.)

    Дополнительные примеры настройки различных свойств для удаленного подключения WMI см. в разделе "примеры" на странице справочника по [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .

## <a name="microsoftmanagementinfrastructure-example"></a>Пример Microsoft. Management. Infrastructure

Следующий пример кода C#, основанный на следующей [записи блога на TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), описывает, как использовать [Цимкредентиалс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) и [всмансессионоптионс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) для установки учетных данных на удаленном подключении.


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



## <a name="systemmanagement-example"></a>Пример System. Management

В следующем образце кода C# описывается общее удаленное подключение с помощью объектов System. Management.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
