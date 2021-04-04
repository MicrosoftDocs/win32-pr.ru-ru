---
description: Дополнительные сведения о методе API. Жеттрункателогинстанце
title: API. Жеттрункателогинстанце, метод
TOCTitle: 'JetTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jettruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55100815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc1693b3f84cd594bfeca81a8e854e49e28d955f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999548"
---
# <a name="apijettruncateloginstance-method"></a><span data-ttu-id="3d299-103">API. Жеттрункателогинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="3d299-103">Api.JetTruncateLogInstance method</span></span>

<span data-ttu-id="3d299-104">Используется во время резервного копирования, инициированного Жетбегинекстерналбаккуп, для удаления всех файлов журнала транзакций, которые больше не понадобятся после успешного завершения текущего резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="3d299-104">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="3d299-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d299-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d299-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d299-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d299-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d299-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTruncateLogInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTruncateLogInstance(instance)
```

``` csharp
public static void JetTruncateLogInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="3d299-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d299-108">Parameters</span></span>

  - <span data-ttu-id="3d299-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="3d299-109">instance</span></span>  
    <span data-ttu-id="3d299-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3d299-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="3d299-111">Экземпляр для усечения.</span><span class="sxs-lookup"><span data-stu-id="3d299-111">The instance to truncate.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d299-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d299-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d299-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="3d299-113">Reference</span></span>

[<span data-ttu-id="3d299-114">Класс API</span><span class="sxs-lookup"><span data-stu-id="3d299-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3d299-115">Члены API</span><span class="sxs-lookup"><span data-stu-id="3d299-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3d299-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3d299-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
