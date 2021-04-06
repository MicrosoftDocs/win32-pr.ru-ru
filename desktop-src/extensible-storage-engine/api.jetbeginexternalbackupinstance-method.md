---
description: Дополнительные сведения о методе API. Жетбегинекстерналбаккупинстанце
title: API. Жетбегинекстерналбаккупинстанце, метод
TOCTitle: 'JetBeginExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100659
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c42f5d1f62de0af7582247fb47d407f82981a42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991000"
---
# <a name="apijetbeginexternalbackupinstance-method"></a><span data-ttu-id="feb01-103">API. Жетбегинекстерналбаккупинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="feb01-103">Api.JetBeginExternalBackupInstance method</span></span>

<span data-ttu-id="feb01-104">Инициирует внешнюю архивацию, пока ядро и база данных находятся в сети и активны.</span><span class="sxs-lookup"><span data-stu-id="feb01-104">Initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="feb01-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="feb01-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="feb01-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="feb01-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="feb01-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="feb01-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginExternalBackupInstance ( _
    instance As JET_INSTANCE, _
    grbit As BeginExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As BeginExternalBackupGrbitApi.JetBeginExternalBackupInstance(instance, _
    grbit)
```

``` csharp
public static void JetBeginExternalBackupInstance(
    JET_INSTANCE instance,
    BeginExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="feb01-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="feb01-108">Parameters</span></span>

  - <span data-ttu-id="feb01-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="feb01-109">instance</span></span>  
    <span data-ttu-id="feb01-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="feb01-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="feb01-111">Экземпляр, подготавливается к резервному копированию.</span><span class="sxs-lookup"><span data-stu-id="feb01-111">The instance prepare for backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="feb01-112">грбит</span><span class="sxs-lookup"><span data-stu-id="feb01-112">grbit</span></span>  
    <span data-ttu-id="feb01-113">Тип: [Microsoft. ISAM. ESENT. Interop. бегинекстерналбаккупгрбит](./beginexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="feb01-113">Type: [Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="feb01-114">Параметры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="feb01-114">Backup options.</span></span>

## <a name="see-also"></a><span data-ttu-id="feb01-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feb01-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="feb01-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="feb01-116">Reference</span></span>

[<span data-ttu-id="feb01-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="feb01-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="feb01-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="feb01-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="feb01-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="feb01-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
