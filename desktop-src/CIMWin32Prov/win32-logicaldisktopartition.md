---
description: '\_Класс WMI взаимосвязей Win32 логикалдисктопартитион связывает логический диск и раздел диска, на котором он находится.'
ms.assetid: 41161d57-d392-4acc-a22a-10be75aa14a6
ms.tgt_platform: multiple
title: Класс Win32_LogicalDiskToPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskToPartition
- Win32_LogicalDiskToPartition.EndingAddress
- Win32_LogicalDiskToPartition.StartingAddress
- Win32_LogicalDiskToPartition.Antecedent
- Win32_LogicalDiskToPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a32a3ee275c32dde7d9f1484aa99dddeaf97a2e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140979"
---
# <a name="win32_logicaldisktopartition-class"></a><span data-ttu-id="38992-103">\_Класс Win32 логикалдисктопартитион</span><span class="sxs-lookup"><span data-stu-id="38992-103">Win32\_LogicalDiskToPartition class</span></span>

<span data-ttu-id="38992-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ логикалдисктопартитион** связывает логический диск и раздел диска, на котором он находится.</span><span class="sxs-lookup"><span data-stu-id="38992-104">The **Win32\_LogicalDiskToPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk drive and the disk partition it resides on.</span></span>

<span data-ttu-id="38992-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="38992-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="38992-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="38992-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38992-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38992-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDiskToPartition : CIM_LogicalDiskBasedOnPartition
{
  uint64                  EndingAddress;
  uint64                  StartingAddress;
  Win32_DiskPartition REF Antecedent;
  Win32_LogicalDisk   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="38992-108">Члены</span><span class="sxs-lookup"><span data-stu-id="38992-108">Members</span></span>

<span data-ttu-id="38992-109">Класс **Win32 \_ логикалдисктопартитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38992-109">The **Win32\_LogicalDiskToPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="38992-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="38992-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38992-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="38992-111">Properties</span></span>

<span data-ttu-id="38992-112">Класс **Win32 \_ логикалдисктопартитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38992-112">The **Win32\_LogicalDiskToPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38992-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="38992-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38992-114">Тип данных: **Win32 \_ дискпартитион**</span><span class="sxs-lookup"><span data-stu-id="38992-114">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="38992-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38992-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38992-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дискпартитион")</span><span class="sxs-lookup"><span data-stu-id="38992-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="38992-117">Ссылка на экземпляр, представляющий свойства раздела диска, в котором находится логический диск.</span><span class="sxs-lookup"><span data-stu-id="38992-117">Reference to the instance representing the properties of a disk partition where the logical disk resides.</span></span>

</dd> <dt>

<span data-ttu-id="38992-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="38992-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38992-119">Тип данных: **Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="38992-119">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="38992-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38992-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38992-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")</span><span class="sxs-lookup"><span data-stu-id="38992-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="38992-122">Ссылка на экземпляр, представляющий свойства логического диска, находящегося в разделе физического диска.</span><span class="sxs-lookup"><span data-stu-id="38992-122">Reference to the instance representing the properties of a logical disk that resides on a physical disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="38992-123">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="38992-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38992-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38992-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38992-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38992-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38992-126">Указывает конец высокоуровневого экстента в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="38992-126">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="38992-127">Это свойство полезно при сопоставлении несмежных экстентов с группировкой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="38992-127">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="38992-128">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="38992-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="38992-129">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="38992-129">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="38992-130">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="38992-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38992-131">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38992-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38992-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38992-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38992-133">Указывает начало экстента высокого уровня в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="38992-133">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="38992-134">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="38992-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="38992-135">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="38992-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38992-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38992-136">Remarks</span></span>

<span data-ttu-id="38992-137">Класс **Win32 \_ логикалдисктопартитион** является производным от [**CIM \_ логикалдискбаседонпартитион**](cim-logicaldiskbasedonpartition.md).</span><span class="sxs-lookup"><span data-stu-id="38992-137">The **Win32\_LogicalDiskToPartition** class is derived from [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md).</span></span>

<span data-ttu-id="38992-138">Дополнительные сведения о сопоставлении между логическим диском и физическим диском см. в разделе [как можно сопоставить логические диски и физические диски?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx)</span><span class="sxs-lookup"><span data-stu-id="38992-138">For more information on mapping between a logical drive and a physical disk, see [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="38992-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="38992-139">Examples</span></span>

<span data-ttu-id="38992-140">В следующем примере кода C++ показано, как получить буквы дисков для указанного диска.</span><span class="sxs-lookup"><span data-stu-id="38992-140">The following C++ code sample describes how to retrieve the drive letters for a specified disk drive.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>


#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")


  
BOOL wmi_run();
BOOL wmi_getDriveLetters();
BOOL wmi_close();


  
IWbemLocator *pLoc = NULL;
IWbemServices *pSvc = NULL;


  
int main(int argc, char **argv)
{
    wmi_run();
    wmi_getDriveLetters();

    system("pause");
    wmi_close();
}


  
//
// Step 1-5 at:
// https://msdn.microsoft.com/library/aa390423(VS.85).aspx
BOOL wmi_run()
{
     HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------
    // Note: If you are using Windows 2000, you need to specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );


  
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }

    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    //IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);

    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    //IWbemServices *pSvc = NULL;

    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (e.g. Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );

    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;

    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
 return 0;
}


  
//
// get Drives, logical Drives and Driveletters
BOOL wmi_getDriveLetters()
{

    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:
    HRESULT hres;
    IEnumWbemClassObject* pEnumerator = NULL;

    // get localdrives
    hres = pSvc->ExecQuery(
                    bstr_t("WQL"), 
                    bstr_t("SELECT * FROM Win32_DiskDrive"),
                    WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                    NULL,
                    &pEnumerator);

    if (FAILED(hres)) {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return FALSE;               // Program has failed.
    }
    else { 

        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
        while (pEnumerator) {
           hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                                 &pclsObj, &uReturn);
           if(0 == uReturn) break;

           VARIANT vtProp;
           hres = pclsObj->Get(_bstr_t(L"DeviceID"), 0, &vtProp, 0, 0);

           // adjust string
           wstring tmp = vtProp.bstrVal;
           tmp = tmp.substr(4);

           wstring wstrQuery = L"Associators of {Win32_DiskDrive.DeviceID='\\\\.\\";
           wstrQuery += tmp;
           wstrQuery += L"'} where AssocClass=Win32_DiskDriveToDiskPartition";

           // reference drive to partition
           IEnumWbemClassObject* pEnumerator1 = NULL;
           hres = pSvc->ExecQuery(
                             bstr_t("WQL"), 
                             bstr_t( wstrQuery.c_str()),
                             WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                             NULL,
                             &pEnumerator1 );

           if ( FAILED(hres) ) {
            cout << "Query for processes failed. "
                          << "Error code = 0x" 
                          << hex << hres << endl;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return FALSE;               // Program has failed.
           } else {

                IWbemClassObject *pclsObj1;
                ULONG uReturn1 = 0;
                while( pEnumerator1 ) {
                     hres = pEnumerator1->Next( WBEM_INFINITE, 1, 
                     &pclsObj1, &uReturn1 );
                     if(0 == uReturn1) break;

                     // reference logical drive to partition
                     VARIANT vtProp1;
                     hres = pclsObj1->Get( _bstr_t(L"DeviceID"), 0, &vtProp1, 0, 0 );
                     wstring wstrQuery = L"Associators of {Win32_DiskPartition.DeviceID='";
                     wstrQuery += vtProp1.bstrVal;
                     wstrQuery += L"'} where AssocClass=Win32_LogicalDiskToPartition";


  
                     IEnumWbemClassObject* pEnumerator2 = NULL;
                     hres = pSvc->ExecQuery(
                                       bstr_t("WQL"), 
                                       bstr_t(wstrQuery.c_str()),
                                       WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                                       NULL,
                                       &pEnumerator2 );





                    if ( FAILED(hres) ) {
                        cout << "Query for processes failed. "
                                << "Error code = 0x" 
                                << hex << hres << endl;
                        pSvc->Release();
                        pLoc->Release();     
                        CoUninitialize();
                        return FALSE;               // Program has failed.
                     } else {

                        // get driveletter
                        IWbemClassObject *pclsObj2;
                        ULONG uReturn2 = 0;
                        while( pEnumerator2 ) {
                            hres = pEnumerator2->Next( WBEM_INFINITE, 1, 
                            &pclsObj2, &uReturn2 );
                            if(0 == uReturn2) break;

                            VARIANT vtProp2;
                            hres = pclsObj2->Get( _bstr_t(L"DeviceID"), 0, &vtProp2, 0, 0 );


  
                            // print result
                            printf("%ls : %ls\n", vtProp.bstrVal, vtProp2.bstrVal);

                            VariantClear( &vtProp2 );
                        }
                        pclsObj1->Release();
                    }
                    VariantClear( &vtProp1 );
                    pEnumerator2->Release();
                }
                pclsObj->Release();
            }
            VariantClear( &vtProp );
            pEnumerator1->Release();
        }
     }
     pEnumerator->Release();
     return TRUE;
}






BOOL wmi_close()
{
 // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed. 
}
```



## <a name="requirements"></a><span data-ttu-id="38992-141">Требования</span><span class="sxs-lookup"><span data-stu-id="38992-141">Requirements</span></span>



| <span data-ttu-id="38992-142">Требование</span><span class="sxs-lookup"><span data-stu-id="38992-142">Requirement</span></span> | <span data-ttu-id="38992-143">Значение</span><span class="sxs-lookup"><span data-stu-id="38992-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38992-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38992-144">Minimum supported client</span></span><br/> | <span data-ttu-id="38992-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38992-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38992-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38992-146">Minimum supported server</span></span><br/> | <span data-ttu-id="38992-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38992-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38992-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38992-148">Namespace</span></span><br/>                | <span data-ttu-id="38992-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="38992-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38992-150">MOF</span><span class="sxs-lookup"><span data-stu-id="38992-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38992-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38992-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38992-152">DLL</span><span class="sxs-lookup"><span data-stu-id="38992-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38992-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38992-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38992-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38992-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38992-155">**\_ЛОГИКАЛДИСКБАСЕДОНПАРТИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="38992-155">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dt>

<span data-ttu-id="38992-156">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38992-156">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="38992-157">Задачи WMI: диски и файловые системы</span><span class="sxs-lookup"><span data-stu-id="38992-157">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

