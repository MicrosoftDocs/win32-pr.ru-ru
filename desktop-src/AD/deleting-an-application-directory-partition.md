---
title: Удаление раздела каталога приложений
description: Раздел каталога приложений удаляется путем удаления объекта crossRef, представляющего раздел каталога приложений.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Удаление раздела каталога приложений
- Разделы каталога приложений AD, удаление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789582"
---
# <a name="deleting-an-application-directory-partition"></a><span data-ttu-id="4f279-105">Удаление раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="4f279-105">Deleting an Application Directory Partition</span></span>

<span data-ttu-id="4f279-106">Раздел каталога приложений удаляется путем удаления объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) , представляющего раздел каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="4f279-106">An application directory partition is deleted by deleting the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition.</span></span> <span data-ttu-id="4f279-107">При репликации объекта **crossRef** на контроллер домена с репликой раздела каталога приложений KCC удаляет локальную реплику раздела каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="4f279-107">When the deletion of the **crossRef** object replicates to a domain controller that has a replica of the application directory partition, the KCC will delete the local replica of the application directory partition.</span></span> <span data-ttu-id="4f279-108">В итоге будут удалены все реплики раздела каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="4f279-108">This eventually causes all replicas of the application directory partition to be deleted.</span></span>

<span data-ttu-id="4f279-109">При удалении объекта [**crossRef**](/windows/desktop/ADSchema/c-crossref) сервер Active Directory удаляет объект [**домаинднс**](/windows/desktop/ADSchema/c-domaindns) , который был создан при создании раздела каталога приложений, а также удаляет все объекты в разделе каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="4f279-109">When the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is deleted, the Active Directory server will delete the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object that was created when the application directory partition was created, as well as deleting all objects in the application directory partition.</span></span> <span data-ttu-id="4f279-110">Ни один из объектов в разделе каталога приложений не захоронен при удалении.</span><span class="sxs-lookup"><span data-stu-id="4f279-110">None of the objects in the application directory partition are tombstoned when they deleted.</span></span>

<span data-ttu-id="4f279-111">При удалении раздела каталога приложений очень сложно его восстановить.</span><span class="sxs-lookup"><span data-stu-id="4f279-111">When an application directory partition is deleted, it is very difficult to restore it.</span></span> <span data-ttu-id="4f279-112">Чтобы восстановить раздел каталога приложений, необходимо восстановить резервную копию, которая содержит реплику раздела каталога приложений, найти объект [**crossRef**](/windows/desktop/ADSchema/c-crossref) , представляющий раздел каталога приложений, и принудительно восстановить объект **crossRef** .</span><span class="sxs-lookup"><span data-stu-id="4f279-112">To restore an application directory partition, it is necessary to restore a backup that has a replica of the application directory partition, find the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and authoritatively restore the **crossRef** object.</span></span>

<span data-ttu-id="4f279-113">**Чтобы удалить раздел каталога приложения и его реплики, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="4f279-113">**To delete an application directory partition and its replicas, perform the following steps**</span></span>

1.  <span data-ttu-id="4f279-114">Найдите в контейнере секций объект [**crossRef**](/windows/desktop/ADSchema/c-crossref) , имеющий значение атрибута [**NCName**](/windows/desktop/ADSchema/a-ncname) , равное различающихся именам разделов каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="4f279-114">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="4f279-115">Удалите объект [**crossRef**](/windows/desktop/ADSchema/c-crossref) .</span><span class="sxs-lookup"><span data-stu-id="4f279-115">Delete the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="4f279-116">Дополнительные сведения см. в разделе [пример кода для удаления раздела каталога приложений](example-code-for-deleting-an-application-directory-partition.md).</span><span class="sxs-lookup"><span data-stu-id="4f279-116">For more information, see [Example Code for Deleting an Application Directory Partition](example-code-for-deleting-an-application-directory-partition.md).</span></span>

 

 