---
description: В качестве альтернативы созданию и настройке локальных секций с помощью средства администрирования "службы компонентов" можно управлять разделами программным способом с помощью отдельных разделов и свойств администрирования COM+.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Управление локальными секциями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124d0b9ef7bf54f07a6b28561428c57834a6e15ec11c4ed5c89fb92f95f0a950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306265"
---
# <a name="managing-local-partitions"></a>Управление локальными секциями

В качестве альтернативы созданию и настройке локальных секций с помощью средства администрирования "службы компонентов" можно управлять разделами программным способом с помощью отдельных разделов и свойств администрирования COM+.

> [!Note]  
> Служба "разделы COM+" не включена по умолчанию. Чтобы использовать службу "разделы COM+", необходимо включить ее с помощью средства администрирования служб компонентов или путем изменения свойства Партитионсенаблед в коллекции [**локалкомпутер**](localcomputer.md) на true.

 

следующая подпроцедура, написанная на Visual Basic скрипте, демонстрирует создание раздела на локальном компьютере:


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



в следующей подпроцедуре, написанной в Visual Basic скрипте, показано, как удалить раздел с локального компьютера:


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



в следующей подпроцедуре, написанной в Visual Basic скрипте, показано, как задать раздел по умолчанию для пользователя:


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



в следующей подпроцедуре, написанной в Visual Basic скрипте, показано, как удалить секцию по умолчанию для пользователя:


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сбор метрик секции](collecting-partition-metrics.md)
</dt> <dt>

[Настройка кэша секций](configuring-the-partition-cache.md)
</dt> <dt>

[Группирование приложений в секции](grouping-applications-into-partitions.md)
</dt> <dt>

[Управление секциями в Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Установка прав администратора для секции](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



