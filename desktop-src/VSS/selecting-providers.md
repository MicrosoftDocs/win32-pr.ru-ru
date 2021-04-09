---
description: Инициатор запроса должен выбрать конкретного поставщика, только если у него есть некоторые сведения о доступных поставщиках.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Выбор поставщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156102"
---
# <a name="selecting-providers"></a><span data-ttu-id="63934-103">Выбор поставщиков</span><span class="sxs-lookup"><span data-stu-id="63934-103">Selecting Providers</span></span>

<span data-ttu-id="63934-104">Инициатор запроса должен выбрать конкретного поставщика, только если у него есть некоторые сведения о доступных поставщиках.</span><span class="sxs-lookup"><span data-stu-id="63934-104">A requester should select a specific provider only if it has some information about the providers available.</span></span>

<span data-ttu-id="63934-105">Так как это обычно не так, рекомендуется предоставить идентификатор GUID в \_ качестве идентификатора поставщика для [**ивссбаккупкомпонентс:: аддтоснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), который позволяет системе выбрать поставщик в соответствии со следующим алгоритмом:</span><span class="sxs-lookup"><span data-stu-id="63934-105">Because this will not generally be the case, it is recommended that a requester supply GUID\_NULL as a provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), which allows the system to choose a provider according to the following algorithm:</span></span>

1.  <span data-ttu-id="63934-106">Если поставщик оборудования, поддерживающий данный том, доступен, он выбирается.</span><span class="sxs-lookup"><span data-stu-id="63934-106">If a hardware provider that supports the given volume is available, it is selected.</span></span>
2.  <span data-ttu-id="63934-107">Если поставщик оборудования недоступен, то в случае доступности любого поставщика программного обеспечения, относящегося к данному тому, он будет выбран.</span><span class="sxs-lookup"><span data-stu-id="63934-107">If no hardware provider is available, then if any software provider specific to the given volume is available, it is selected.</span></span>
3.  <span data-ttu-id="63934-108">Если поставщик оборудования и поставщик программного обеспечения не доступны для томов, то выбран поставщик системы.</span><span class="sxs-lookup"><span data-stu-id="63934-108">If no hardware provider and no software provider specific to the volumes is available, the system provider is selected.</span></span>

<span data-ttu-id="63934-109">Однако инициатор запроса может получить сведения о доступных поставщиках с помощью [**ивссбаккупкомпонентс:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="63934-109">However, a requester can obtain information about available providers by using [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span> <span data-ttu-id="63934-110">С помощью этой информации и только в том случае, если приложение резервного копирования имеет хорошее представление о различных поставщиках, инициатор запроса может предоставить действительный идентификатор поставщика [**ивссбаккупкомпонентс:: аддтоснапшотсет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span><span class="sxs-lookup"><span data-stu-id="63934-110">With this information, and only if the backup application has a good understanding of the various providers, a requester can supply a valid provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="63934-111">Обратите внимание, что все тома не должны иметь одного и того же поставщика.</span><span class="sxs-lookup"><span data-stu-id="63934-111">Note that all volumes do not need to have the same provider.</span></span>

 

 



