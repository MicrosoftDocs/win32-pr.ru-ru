---
description: 'Во время операции восстановления инициатор запроса может использовать метод Ивссбаккупкомпонентс:: Сетресторестате для определения типа выполняемой операции восстановления.'
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: Состояние восстановления VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692367"
---
# <a name="vss-restore-state"></a><span data-ttu-id="86732-103">Состояние восстановления VSS</span><span class="sxs-lookup"><span data-stu-id="86732-103">VSS Restore State</span></span>

<span data-ttu-id="86732-104">Во время операции восстановления инициатор запроса может использовать метод [**ивссбаккупкомпонентс:: сетресторестате**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) для определения типа выполняемой операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="86732-104">During a restore operation, the requester can use the [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) method to define the type of restore operation in progress.</span></span> <span data-ttu-id="86732-105">Однако большинству операций восстановления не требуется переопределять тип восстановления по умолчанию (VSS \_ ртипе \_ undefine).</span><span class="sxs-lookup"><span data-stu-id="86732-105">However, most restore operations will not need to override the default restore type (VSS\_RTYPE\_UNDEFINED).</span></span> <span data-ttu-id="86732-106">Модули записи должны считать этот тип восстановления, как если бы он был \_ РТИПЕ VSS \_ по \_ копированию.</span><span class="sxs-lookup"><span data-stu-id="86732-106">Writers should treat this restore type as if it were VSS\_RTYPE\_BY\_COPY.</span></span> <span data-ttu-id="86732-107">Дополнительные сведения о значениях типов восстановления см. в разделе Перечисление [**\_ \_ типов восстановления VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .</span><span class="sxs-lookup"><span data-stu-id="86732-107">For more information about restore type values, see the [**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) enumeration.</span></span>

 

 



