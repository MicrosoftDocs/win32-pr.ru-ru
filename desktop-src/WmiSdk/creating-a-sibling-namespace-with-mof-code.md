---
description: Другим способом создания пространства имен является использование MOF-файл (MOF) кода для создания пространства имен одного уровня. Пространство имен одного уровня — это пространство имен, которое не существует в качестве дочернего для текущего пространства имен.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Создание родственного пространства имен с помощью MOF-кода
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651122"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a><span data-ttu-id="2c97f-104">Создание родственного пространства имен с помощью MOF-кода</span><span class="sxs-lookup"><span data-stu-id="2c97f-104">Creating a Sibling Namespace with MOF Code</span></span>

<span data-ttu-id="2c97f-105">Другим способом создания пространства имен является использование MOF-файл (MOF) кода для создания пространства имен одного уровня.</span><span class="sxs-lookup"><span data-stu-id="2c97f-105">Another way of creating a namespace is to use Managed Object Format (MOF) code to create a sibling namespace.</span></span> <span data-ttu-id="2c97f-106">Пространство имен одного уровня — это пространство имен, которое не существует в качестве дочернего для текущего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2c97f-106">A sibling namespace is a namespace that does not exist as a child of the current namespace.</span></span>

<span data-ttu-id="2c97f-107">В следующей процедуре описывается создание пространства имен с общим пространством с помощью MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="2c97f-107">The following procedure describes how to create a sibling namespace with MOF code.</span></span>

<span data-ttu-id="2c97f-108">**Создание пространства имен с общим пространством с помощью MOF-кода**</span><span class="sxs-lookup"><span data-stu-id="2c97f-108">**To create a sibling namespace with MOF code**</span></span>

1.  <span data-ttu-id="2c97f-109">Перед объявлением пространства имен вставьте команду [**\# pragma Namespace**](pragma-namespace.md) в свой MOF-код.</span><span class="sxs-lookup"><span data-stu-id="2c97f-109">Insert the [**\#pragma namespace**](pragma-namespace.md) command into your MOF code prior to the namespace declaration.</span></span>

    <span data-ttu-id="2c97f-110">Команда [**\# pragma Namespace**](pragma-namespace.md) указывает инструментарию WMI, где создавать экземпляры после директивы.</span><span class="sxs-lookup"><span data-stu-id="2c97f-110">The [**\#pragma namespace**](pragma-namespace.md) command instructs WMI where to create the instances following the directive.</span></span>

2.  <span data-ttu-id="2c97f-111">Создайте экземпляр класса [**\_ \_ Namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="2c97f-111">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>
3.  <span data-ttu-id="2c97f-112">Скомпилируйте код с помощью программы [mofcomp](mofcomp.md) или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="2c97f-112">Compile your code with the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="2c97f-113">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="2c97f-113">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="2c97f-114">В следующем примере MOF-кода показано, как создать пространство имен в качестве одноуровневого элемента для \\ пространства имен root CIMv2.</span><span class="sxs-lookup"><span data-stu-id="2c97f-114">The following MOF code example describes how to create a namespace as a sibling to the "Root\\CIMv2" namespace.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



