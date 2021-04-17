---
title: Настройка безопасности при создании пространства имен
description: Файл MOF-файл (MOF), который создает пространство имен, также может определять дескрипторы безопасности для пространства имен, включая квалификатор Намеспацесекуритисддл с дескриптором безопасности в формате языка определения дескрипторов безопасности (SDDL).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546874"
---
# <a name="setting-security-on-namespace-creation"></a><span data-ttu-id="22acd-103">Настройка безопасности при создании пространства имен</span><span class="sxs-lookup"><span data-stu-id="22acd-103">Setting security on namespace creation</span></span>

<span data-ttu-id="22acd-104">Файл MOF-файл (MOF), который создает пространство имен, также может определять [*дескрипторы безопасности*](/windows/desktop/SecGloss/s-gly) для пространства имен, включая квалификатор **намеспацесекуритисддл** с дескриптором безопасности в формате [языка определения дескрипторов безопасности (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="22acd-104">The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](/windows/desktop/SecGloss/s-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span>

<span data-ttu-id="22acd-105">**Намеспацесекуритисддл** можно использовать для защиты любого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="22acd-105">You can use **NamespaceSecuritySDDL** to secure any namespace.</span></span> <span data-ttu-id="22acd-106">Этот квалификатор также можно использовать в простом MOF-файле для изменения дескриптора безопасности существующего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="22acd-106">You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace.</span></span> <span data-ttu-id="22acd-107">Строка SDDL обрабатывается WMI для установления безопасности пространства имен, но не хранится в виде строки.</span><span class="sxs-lookup"><span data-stu-id="22acd-107">The SDDL string is processed by WMI to establish the namespace security but is not stored as a string.</span></span> <span data-ttu-id="22acd-108">Если дескриптор безопасности не указан, используется безопасность по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22acd-108">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="22acd-109">Дополнительные сведения см. в разделе [Настройка дескрипторов безопасности намепаце](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="22acd-109">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="22acd-110">Следующая процедура задает дескриптор безопасности для *корневого пространства имен \\ MyNamespace* .</span><span class="sxs-lookup"><span data-stu-id="22acd-110">The following procedure sets the security descriptor for the *root\\MyNamespace* namespace.</span></span> <span data-ttu-id="22acd-111">Строка SDDL задает владельца и группу для пользователей, прошедших проверку подлинности, и указывает [*список управления доступом на уровне пользователей (DACL)*](/windows/desktop/SecGloss/d-gly) , наследуемый дочерними пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="22acd-111">The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) that is inherited by child namespaces.</span></span> <span data-ttu-id="22acd-112">DACL позволяет пользователю читать данные, выполнять методы, записывать данные в классы поставщиков и использовать удаленный доступ: **\_ Enable WBEM**, **\_ \_ выполнение метода WBEM**, **\_ \_ поставщик записи WBEM**, **\_ Удаленный \_ доступ WBEM**.</span><span class="sxs-lookup"><span data-stu-id="22acd-112">The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**.</span></span> <span data-ttu-id="22acd-113">Дополнительные сведения см. [в разделе доступ к пространствам имен WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="22acd-113">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="22acd-114">**Задание DACL пространства имен**</span><span class="sxs-lookup"><span data-stu-id="22acd-114">**To set a namespace DACL**</span></span>

1.  <span data-ttu-id="22acd-115">Создайте файл MOF-файл (MOF) или измените существующий MOF-файл, определяющий пространство имен, чтобы добавить квалификатор **намеспацесекуритисддл** со строкой SDDL.</span><span class="sxs-lookup"><span data-stu-id="22acd-115">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.</span></span>

    <span data-ttu-id="22acd-116">В следующем примере кода показано пространство имен, которое необходимо изменить, — root \\ MyNamespace, а файлу — MyNamespace \_ Security. mof.</span><span class="sxs-lookup"><span data-stu-id="22acd-116">The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  <span data-ttu-id="22acd-117">Имейте в виду, что строка SDDL учитывает регистр: буквы должны быть прописными буквами.</span><span class="sxs-lookup"><span data-stu-id="22acd-117">Be aware that the SDDL string is case-sensitive: the letters must be capitalized.</span></span>

    <span data-ttu-id="22acd-118">В следующем примере кода показаны буквы "o" и "g" в строке SDDL в нижнем регистре, что приведет к тому, что Mofcomp.exe будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="22acd-118">The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  <span data-ttu-id="22acd-119">Запустите [**Mofcomp.exe**](mofcomp.md) , чтобы скомпилировать MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="22acd-119">Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="22acd-120">**c: \\ mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="22acd-120">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="22acd-121">В C++ используйте методы [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="22acd-121">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

4.  <span data-ttu-id="22acd-122">Если попытка задать DACL пространства имен не удалась, рассмотрите следующие сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="22acd-122">If your attempt to set the namespace DACL fails, consider the following error messages:</span></span>

    

    | <span data-ttu-id="22acd-123">Ошибка</span><span class="sxs-lookup"><span data-stu-id="22acd-123">Error</span></span>                           | <span data-ttu-id="22acd-124">Описание</span><span class="sxs-lookup"><span data-stu-id="22acd-124">Description</span></span>                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="22acd-125">**\_ \_ Недопустимый параметр "WBEM E" \_**</span><span class="sxs-lookup"><span data-stu-id="22acd-125">**WBEM\_E\_INVALID\_PARAMETER**</span></span> | <span data-ttu-id="22acd-126">Унаследованные списки DACL отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="22acd-126">There is no inherited DACL.</span></span> <span data-ttu-id="22acd-127">Кроме того, вызывающий объект нарушает список DACL или SD в родительском пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="22acd-127">Alternately, the caller has violated the DACL or the SD in the parent namespace.</span></span> |
    | <span data-ttu-id="22acd-128">**\_ \_ отказано в доступе к WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="22acd-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>     | <span data-ttu-id="22acd-129">Вызывающий объект не имеет разрешения на обновление SDDL в MOF.</span><span class="sxs-lookup"><span data-stu-id="22acd-129">The caller does not have permission to update the SDDL in MOF.</span></span>                                               |

    

     

## <a name="related-topics"></a><span data-ttu-id="22acd-130">См. также</span><span class="sxs-lookup"><span data-stu-id="22acd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22acd-131">Задание дескрипторов безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="22acd-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="22acd-132">**Константы прав доступа к пространству имен**</span><span class="sxs-lookup"><span data-stu-id="22acd-132">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
</dt> <dt>

[<span data-ttu-id="22acd-133">**Константы флагов пространства имен ACE**</span><span class="sxs-lookup"><span data-stu-id="22acd-133">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
</dt> <dt>

[<span data-ttu-id="22acd-134">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="22acd-134">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
