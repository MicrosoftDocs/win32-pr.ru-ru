---
description: Все классы представлений должны иметь квалификатор массива строк с именем Виевсаурцес.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Квалификатор Виевсаурцес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815369"
---
# <a name="viewsources-qualifier"></a><span data-ttu-id="e2958-103">Квалификатор Виевсаурцес</span><span class="sxs-lookup"><span data-stu-id="e2958-103">ViewSources Qualifier</span></span>

<span data-ttu-id="e2958-104">Все классы представлений должны иметь квалификатор массива строк с именем **виевсаурцес**.</span><span class="sxs-lookup"><span data-stu-id="e2958-104">All view classes must have a string array qualifier called **ViewSources**.</span></span> <span data-ttu-id="e2958-105">Квалификатор **виевсаурцес** содержит исходные запросы, определяющие исходные экземпляры, используемые в классе представления.</span><span class="sxs-lookup"><span data-stu-id="e2958-105">The **ViewSources** qualifier contains the source queries that define the source instances used in the view class.</span></span> <span data-ttu-id="e2958-106">Значение квалификатора **виевсаурцес** — это строковый массив, содержащий запросы [*язык запросов WMI (WQL)*](gloss-w.md) .</span><span class="sxs-lookup"><span data-stu-id="e2958-106">The value of the **ViewSources** qualifier is a string array containing [*WMI Query Language (WQL)*](gloss-w.md) queries.</span></span> <span data-ttu-id="e2958-107">Можно определить исходные классы и ограничить экземпляры источника, используемые классом представления, с [запросом с помощью](querying-with-wql.md)[предложения WHERE](where-clause.md) WQL для создания отфильтрованного представления.</span><span class="sxs-lookup"><span data-stu-id="e2958-107">You can define source classes and restrict the source instances your view class uses with the [Querying with WQL](querying-with-wql.md)[WHERE Clause](where-clause.md) to create a filtered view.</span></span>

<span data-ttu-id="e2958-108">[Поставщик представления](view-provider.md) сопоставляет исходные запросы в квалификаторе **виевсаурцес** с пространствами имен, перечисленными в [квалификаторе виевспацес](viewspaces-qualifier.md) в том порядке, в котором перечислены запросы и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e2958-108">The [View Provider](view-provider.md) matches the source queries in the **ViewSources** qualifier to the namespaces listed in the [ViewSpaces qualifier](viewspaces-qualifier.md) in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="e2958-109">Число исходных запросов должно совпадать с количеством пространств имен, перечисленных в квалификаторе Виевспацес.</span><span class="sxs-lookup"><span data-stu-id="e2958-109">The number of source queries must match the number of namespaces listed in the ViewSpaces qualifier.</span></span> <span data-ttu-id="e2958-110">Порядок, в котором перечисляются исходные запросы, определяет пространства имен, из которых рисуются исходные экземпляры.</span><span class="sxs-lookup"><span data-stu-id="e2958-110">The order in which you list the source queries determines the namespaces from which the source instances are drawn.</span></span>

<span data-ttu-id="e2958-111">В следующем примере выбираются только экземпляры класса **локалдиск** , где значение свойства **FILESYSTEM** равно "NTFS", и экземпляры класса **Ремотедиск** , где значение свойства **Freespace** превышает 45 МБ.</span><span class="sxs-lookup"><span data-stu-id="e2958-111">The following example selects only instances of the **LocalDisk** class where the value of the **FileSystem** property is "NTFS" and instances of the **RemoteDisk** class where the value of the **FreeSpace** property is greater than 45 megabytes:</span></span>


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> <span data-ttu-id="e2958-112">Количество исходных запросов, которые можно определить для классов представления соединения, зависит от числа экземпляров, возвращаемых этими запросами, и от того, сколько способов можно объединить с этими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="e2958-112">The number of source queries you can define for join view classes depends on the number of instances these queries return and how many ways these instances can be joined.</span></span> <span data-ttu-id="e2958-113">Количество возможных сочетаний экземпляров исходного кода для классов представления растет экспоненциально, поэтому необходимо как можно более быстро принимать исходные запросы на соединение с классами представления.</span><span class="sxs-lookup"><span data-stu-id="e2958-113">The number of possible combinations of source instances for view classes grows exponentially, so keep source queries for join view classes as simple as possible.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2958-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e2958-114">Requirements</span></span>



| <span data-ttu-id="e2958-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e2958-115">Requirement</span></span> | <span data-ttu-id="e2958-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e2958-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e2958-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2958-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2958-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2958-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e2958-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2958-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2958-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2958-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2958-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2958-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2958-122">**Квалификаторы, относящиеся к поставщику представления**</span><span class="sxs-lookup"><span data-stu-id="e2958-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




