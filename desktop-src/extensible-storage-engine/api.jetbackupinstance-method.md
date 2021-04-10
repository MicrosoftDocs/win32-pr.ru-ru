---
description: Дополнительные сведения о методе API. Жетбаккупинстанце
title: API. Жетбаккупинстанце, метод
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143363"
---
# <a name="apijetbackupinstance-method"></a><span data-ttu-id="835e7-103">API. Жетбаккупинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="835e7-103">Api.JetBackupInstance method</span></span>

<span data-ttu-id="835e7-104">Выполняет потоковую архивацию экземпляра, включая все подключенные базы данных, в каталог.</span><span class="sxs-lookup"><span data-stu-id="835e7-104">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="835e7-105">При наличии нескольких методов резервного копирования, поддерживаемых ядром, это самая простая и наиболее Инкапсулированная функция.</span><span class="sxs-lookup"><span data-stu-id="835e7-105">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="835e7-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="835e7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="835e7-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="835e7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="835e7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="835e7-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="835e7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="835e7-109">Parameters</span></span>

  - <span data-ttu-id="835e7-110">экземпляр</span><span class="sxs-lookup"><span data-stu-id="835e7-110">instance</span></span>  
    <span data-ttu-id="835e7-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="835e7-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="835e7-112">Экземпляр для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="835e7-112">The instance to backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="835e7-113">ресурс destination</span><span class="sxs-lookup"><span data-stu-id="835e7-113">destination</span></span>  
    <span data-ttu-id="835e7-114">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="835e7-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="835e7-115">Каталог, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="835e7-115">The directory where the backup is to be stored.</span></span> <span data-ttu-id="835e7-116">Если путь резервного копирования имеет значение NULL для использования функции, по возможности будет усекать журналы.</span><span class="sxs-lookup"><span data-stu-id="835e7-116">If the backup path is null to use the function will truncate the logs, if possible.</span></span>

<!-- end list -->

  - <span data-ttu-id="835e7-117">грбит</span><span class="sxs-lookup"><span data-stu-id="835e7-117">grbit</span></span>  
    <span data-ttu-id="835e7-118">Тип: [Microsoft. ISAM. ESENT. Interop. баккупгрбит](./backupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="835e7-118">Type: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="835e7-119">Параметры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="835e7-119">Backup options.</span></span>

<!-- end list -->

  - <span data-ttu-id="835e7-120">статускаллбакк</span><span class="sxs-lookup"><span data-stu-id="835e7-120">statusCallback</span></span>  
    <span data-ttu-id="835e7-121">Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="835e7-121">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="835e7-122">Необязательный обратный вызов уведомления о состоянии.</span><span class="sxs-lookup"><span data-stu-id="835e7-122">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="835e7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="835e7-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="835e7-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="835e7-124">Reference</span></span>

[<span data-ttu-id="835e7-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="835e7-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="835e7-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="835e7-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="835e7-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="835e7-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
