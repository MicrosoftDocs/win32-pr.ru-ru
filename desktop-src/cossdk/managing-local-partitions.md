---
description: В качестве альтернативы созданию и настройке локальных секций с помощью средства администрирования "службы компонентов" можно управлять разделами программным способом с помощью отдельных разделов и свойств администрирования COM+.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Управление локальными секциями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd551fc73c76067c4ab2e988fba79ee702df53c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990754"
---
# <a name="managing-local-partitions"></a><span data-ttu-id="08eba-103">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="08eba-103">Managing Local Partitions</span></span>

<span data-ttu-id="08eba-104">В качестве альтернативы созданию и настройке локальных секций с помощью средства администрирования "службы компонентов" можно управлять разделами программным способом с помощью отдельных разделов и свойств администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="08eba-104">As an alternative to creating and configuring local partitions through the Component Services administrative tool, you can manage partitions programmatically by using partition-specific COM+ administration collections and properties.</span></span>

> [!Note]  
> <span data-ttu-id="08eba-105">Служба "разделы COM+" не включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08eba-105">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="08eba-106">Чтобы использовать службу "разделы COM+", необходимо включить ее с помощью средства администрирования служб компонентов или путем изменения свойства Партитионсенаблед в коллекции [**локалкомпутер**](localcomputer.md) на true.</span><span class="sxs-lookup"><span data-stu-id="08eba-106">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="08eba-107">Следующая подпроцедура, написанная на Visual Basic скрипте, демонстрирует создание раздела на локальном компьютере:</span><span class="sxs-lookup"><span data-stu-id="08eba-107">The following subroutine written in Visual Basic script demonstrates how to create a partition on the local computer:</span></span>


```VB
Sub CreatePartition (PartitonGuid, PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   Set part = collPartitions.Add
   ' If you don't specify a partition GUID, one is created for you.
   ' Otherwise, you can specify one this way:
   part.Value("ID") = PartitonGuid
   part.Value("Name") = PartitionName
   collPartitions.SaveChanges
   Set part = Nothing
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub 
```



<span data-ttu-id="08eba-108">В следующей подпроцедуре, написанной в Visual Basic скрипте, показано, как удалить раздел с локального компьютера:</span><span class="sxs-lookup"><span data-stu-id="08eba-108">The following subroutine written in Visual Basic script demonstrates how to delete a partition from the local computer:</span></span>


```VB
Sub DeletePartition (PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   numPartitions = collPartitions.Count
   ' Begin with the last partition, and work forward through the list.
   For i = numPartitions - 1 To 0 Step -1 
       If collPartitions.Item(i).Value("Name") = PartitionName Then
           collPartitions.Remove i
       End If
   Next
   collPartitions.SaveChanges
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="08eba-109">В следующей подпроцедуре, написанной в Visual Basic скрипте, показано, как задать раздел по умолчанию для пользователя:</span><span class="sxs-lookup"><span data-stu-id="08eba-109">The following subroutine written in Visual Basic script demonstrates how to set the default partition for a user:</span></span>


```VB
Sub SetDefaultPartitionForUser(UserName, PartitionGuid)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   Set user = collUsers.Add
   user.Value("AccountName") = UserName
   user.Value("DefaultPartitionID") = PartitionGuid
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="08eba-110">В следующей подпроцедуре, написанной в Visual Basic скрипте, показано, как удалить секцию по умолчанию для пользователя:</span><span class="sxs-lookup"><span data-stu-id="08eba-110">The following subroutine written in Visual Basic script demonstrates how to remove the default partition for a user:</span></span>


```VB
Sub RemoveDefaultPartitionForUser(UserName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   numUsers = collUsers.Count
   ' Begin with the last user, and work forward through the list.
   For i = numUsers - 1 To 0 Step -1
       If collUsers.Item(i).Value("AccountName") = UserName Then
           collUsers.Remove i
       End If
   Next
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="08eba-111">См. также</span><span class="sxs-lookup"><span data-stu-id="08eba-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08eba-112">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="08eba-112">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="08eba-113">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="08eba-113">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="08eba-114">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="08eba-114">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="08eba-115">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="08eba-115">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="08eba-116">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="08eba-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



