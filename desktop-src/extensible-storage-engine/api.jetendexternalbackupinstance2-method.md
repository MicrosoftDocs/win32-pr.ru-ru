---
description: Дополнительные сведения о методе API. JetEndExternalBackupInstance2
title: API. JetEndExternalBackupInstance2, метод
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262984"
---
# <a name="apijetendexternalbackupinstance2-method"></a><span data-ttu-id="43b2a-103">API. JetEndExternalBackupInstance2, метод</span><span class="sxs-lookup"><span data-stu-id="43b2a-103">Api.JetEndExternalBackupInstance2 method</span></span>

<span data-ttu-id="43b2a-104">Завершает сеанс внешнего резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="43b2a-104">Ends an external backup session.</span></span> <span data-ttu-id="43b2a-105">Этот API является последним в серии API-интерфейсов, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</span><span class="sxs-lookup"><span data-stu-id="43b2a-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="43b2a-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43b2a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43b2a-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43b2a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43b2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43b2a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="43b2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="43b2a-109">Parameters</span></span>

  - <span data-ttu-id="43b2a-110">экземпляр</span><span class="sxs-lookup"><span data-stu-id="43b2a-110">instance</span></span>  
    <span data-ttu-id="43b2a-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43b2a-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="43b2a-112">Экземпляр, для которого завершается резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="43b2a-112">The instance to end the backup for.</span></span>

<!-- end list -->

  - <span data-ttu-id="43b2a-113">грбит</span><span class="sxs-lookup"><span data-stu-id="43b2a-113">grbit</span></span>  
    <span data-ttu-id="43b2a-114">Тип: [Microsoft. ISAM. ESENT. Interop. ендекстерналбаккупгрбит](./endexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="43b2a-114">Type: [Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="43b2a-115">Параметры, определяющие завершение резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="43b2a-115">Options that specify how the backup ended.</span></span>

## <a name="see-also"></a><span data-ttu-id="43b2a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43b2a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43b2a-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="43b2a-117">Reference</span></span>

[<span data-ttu-id="43b2a-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="43b2a-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="43b2a-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="43b2a-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="43b2a-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="43b2a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
