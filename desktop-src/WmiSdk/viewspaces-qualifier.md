---
description: Квалификатор Виевспацес определяет имена и расположение пространств имен, в которых находятся исходные экземпляры. Можно указать любое сочетание пространств имен на локальных или удаленных компьютерах.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Квалификатор Виевспацес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272554"
---
# <a name="viewspaces-qualifier"></a><span data-ttu-id="3d08d-104">Квалификатор Виевспацес</span><span class="sxs-lookup"><span data-stu-id="3d08d-104">ViewSpaces Qualifier</span></span>

<span data-ttu-id="3d08d-105">**Квалификатор виевспацес** определяет имена и расположение пространств имен, в которых находятся исходные экземпляры.</span><span class="sxs-lookup"><span data-stu-id="3d08d-105">The **ViewSpaces qualifier** defines the names and location of the namespaces where the source instances are located.</span></span> <span data-ttu-id="3d08d-106">Можно указать любое сочетание пространств имен на локальных или удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="3d08d-106">You can specify any combination of namespaces on local or remote computers.</span></span>

<span data-ttu-id="3d08d-107">В следующем примере выводится два пространства имен на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3d08d-107">The following example lists two namespaces on the local computer.</span></span>


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



<span data-ttu-id="3d08d-108">[Поставщик представления](view-provider.md) сопоставляет исходные запросы в [квалификаторе виевсаурцес](viewsources-qualifier.md) с пространствами имен, перечисленными в квалификаторе **виевспацес** в том порядке, в котором перечислены запросы и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3d08d-108">The [View provider](view-provider.md) matches the source queries in the [ViewSources qualifier](viewsources-qualifier.md) to the namespaces listed in the **ViewSpaces** qualifier in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="3d08d-109">Как правило, существует связь "один к одному" между числом пространств имен, перечисленных в квалификаторе **виевспацес** , и запросами, перечисленными в квалификаторе **виевсаурцес** .</span><span class="sxs-lookup"><span data-stu-id="3d08d-109">Normally, there is a one-to-one relationship between the number of namespaces listed in the **ViewSpaces** qualifier and the queries listed in the **ViewSources** qualifier.</span></span> <span data-ttu-id="3d08d-110">В некоторых случаях может потребоваться, чтобы запросы, перечисленные в квалификаторе Виевсаурцес, выполнялись в двух или более пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="3d08d-110">In some cases, you may want the queries listed in the ViewSources qualifier to execute against two or more namespaces.</span></span> <span data-ttu-id="3d08d-111">Можно использовать двойное двоеточие "::" для разделения нескольких пространств имен, которые будут оцениваться одним из запросов в массиве **виевсаурцес** .</span><span class="sxs-lookup"><span data-stu-id="3d08d-111">You can use a double colon "::" to separate multiple namespaces that will be evaluated by one of the queries in the **ViewSources** array.</span></span>

<span data-ttu-id="3d08d-112">В следующем примере первый запрос в массиве [**виевсаурцес**](viewsources-qualifier.md) будет выполняться для пространства имен в первой паре кавычек, второй запрос к трем пространствам имен во второй паре кавычек и третий запрос к двум пространствам имен в третьей паре кавычек.</span><span class="sxs-lookup"><span data-stu-id="3d08d-112">In the following example, the first query in the [**ViewSources**](viewsources-qualifier.md) array will be run against the namespace in the first pair of quotes, the second query against the three namespaces in the second pair of quotes, and the third query against the two namespaces in the third pair of quotes.</span></span>


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a><span data-ttu-id="3d08d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3d08d-113">Requirements</span></span>



| <span data-ttu-id="3d08d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3d08d-114">Requirement</span></span> | <span data-ttu-id="3d08d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3d08d-115">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3d08d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d08d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3d08d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d08d-117">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3d08d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d08d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3d08d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d08d-119">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d08d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d08d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d08d-121">**Квалификаторы, относящиеся к поставщику представления**</span><span class="sxs-lookup"><span data-stu-id="3d08d-121">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




