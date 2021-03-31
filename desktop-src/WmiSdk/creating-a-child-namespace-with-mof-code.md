---
description: Самым простым способом создания пространства имен является использование MOF-файл (MOF) кода для создания пространства имен внутри текущего каталога. Текущий каталог определяется при входе в систему.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Создание дочернего пространства имен с помощью MOF-кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104081732"
---
# <a name="creating-a-child-namespace-with-mof-code"></a><span data-ttu-id="4da33-104">Создание дочернего пространства имен с помощью MOF-кода</span><span class="sxs-lookup"><span data-stu-id="4da33-104">Creating a Child Namespace with MOF Code</span></span>

<span data-ttu-id="4da33-105">Самым простым способом создания пространства имен является использование MOF-файл (MOF) кода для создания пространства имен внутри текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="4da33-105">The simplest way of creating a namespace is to use Managed Object Format (MOF) code to create the namespace inside the current directory.</span></span> <span data-ttu-id="4da33-106">Текущий каталог определяется при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="4da33-106">The current directory is defined when you log on.</span></span>

<span data-ttu-id="4da33-107">В следующей процедуре описывается создание дочернего пространства имен с помощью MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="4da33-107">The following procedure describes how to create a child namespace using MOF code.</span></span>

<span data-ttu-id="4da33-108">**Создание дочернего пространства имен с помощью MOF-кода**</span><span class="sxs-lookup"><span data-stu-id="4da33-108">**To create a child namespace using MOF code**</span></span>

1.  <span data-ttu-id="4da33-109">Создайте экземпляр класса [**\_ \_ Namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="4da33-109">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>

    <span data-ttu-id="4da33-110">В следующем примере кода показано, как создать дочернее пространство имен.</span><span class="sxs-lookup"><span data-stu-id="4da33-110">The following code example shows how to create a child namespace.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  <span data-ttu-id="4da33-111">Если требуется, чтобы пользователь имел зашифрованное соединение с пространством имен, используйте квалификатор **рекуиресенкриптион** .</span><span class="sxs-lookup"><span data-stu-id="4da33-111">If you want to require the user to make an encrypted connection to the namespace, use the **RequiresEncryption** qualifier.</span></span> <span data-ttu-id="4da33-112">Дополнительные сведения см. в разделе [требуется зашифрованное соединение с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="4da33-112">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

    <span data-ttu-id="4da33-113">В следующем примере кода показано, как запросить зашифрованное соединение.</span><span class="sxs-lookup"><span data-stu-id="4da33-113">The following code example shows how to require an encrypted connection.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  <span data-ttu-id="4da33-114">Если вы хотите задать дескриптор безопасности в пространстве имен, а не использовать безопасность пространства имен по умолчанию, используйте квалификатор **намеспацесекуритисддл** .</span><span class="sxs-lookup"><span data-stu-id="4da33-114">If you want to set a security descriptor on the namespace rather than using the default namespace security, use the **NamespaceSecuritySDDL** qualifier.</span></span> <span data-ttu-id="4da33-115">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен при создании пространства имен](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="4da33-115">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

    <span data-ttu-id="4da33-116">В следующем примере кода показано, как задать дескриптор безопасности для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4da33-116">The following code example shows how to set a security descriptor on the namespace.</span></span>

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  <span data-ttu-id="4da33-117">Скомпилируйте и загрузите экземпляр [**\_ \_ пространства имен**](--namespace.md) с помощью программы [mofcomp](mofcomp.md) или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="4da33-117">Compile and load the [**\_\_Namespace**](--namespace.md) instance using the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span> <span data-ttu-id="4da33-118">Как mofcomp, так и интерфейс **имофкомпилер** автоматически загружают пространство имен в текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="4da33-118">Both mofcomp and the **IMofCompiler** interface automatically load the namespace into the current directory.</span></span> <span data-ttu-id="4da33-119">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="4da33-119">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4da33-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4da33-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da33-121">**Стандартные квалификаторы WMI**</span><span class="sxs-lookup"><span data-stu-id="4da33-121">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



