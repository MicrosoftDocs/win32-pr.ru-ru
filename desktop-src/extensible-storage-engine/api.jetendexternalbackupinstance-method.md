---
description: Дополнительные сведения о методе API. Жетендекстерналбаккупинстанце
title: API. Жетендекстерналбаккупинстанце, метод
TOCTitle: 'JetEndExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100691
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16ec4dc235f677ba42b4ae3bae10a79b9d494576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990995"
---
# <a name="apijetendexternalbackupinstance-method"></a><span data-ttu-id="5b1ea-103">API. Жетендекстерналбаккупинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="5b1ea-103">Api.JetEndExternalBackupInstance method</span></span>

<span data-ttu-id="5b1ea-104">Завершает сеанс внешнего резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5b1ea-104">Ends an external backup session.</span></span> <span data-ttu-id="5b1ea-105">Этот API является последним в серии API-интерфейсов, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).</span><span class="sxs-lookup"><span data-stu-id="5b1ea-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="5b1ea-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b1ea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5b1ea-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5b1ea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1ea-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b1ea-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetEndExternalBackupInstance(instance)
```

``` csharp
public static void JetEndExternalBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="5b1ea-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b1ea-109">Parameters</span></span>

  - <span data-ttu-id="5b1ea-110">экземпляр</span><span class="sxs-lookup"><span data-stu-id="5b1ea-110">instance</span></span>  
    <span data-ttu-id="5b1ea-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5b1ea-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="5b1ea-112">Экземпляр, для которого завершается резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="5b1ea-112">The instance to end the backup for.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b1ea-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b1ea-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b1ea-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="5b1ea-114">Reference</span></span>

[<span data-ttu-id="5b1ea-115">Класс API</span><span class="sxs-lookup"><span data-stu-id="5b1ea-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5b1ea-116">Члены API</span><span class="sxs-lookup"><span data-stu-id="5b1ea-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5b1ea-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5b1ea-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
