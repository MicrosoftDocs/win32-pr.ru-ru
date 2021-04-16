---
description: Дополнительные сведения о методе API. Жетрестореинстанце
title: API. Жетрестореинстанце, метод
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692211"
---
# <a name="apijetrestoreinstance-method"></a><span data-ttu-id="6601f-103">API. Жетрестореинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="6601f-103">Api.JetRestoreInstance method</span></span>

<span data-ttu-id="6601f-104">Восстанавливает и восстанавливает потоковую передачу резервной копии экземпляра, включая все подключенные базы данных.</span><span class="sxs-lookup"><span data-stu-id="6601f-104">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="6601f-105">Он предназначен для работы с резервной копией, созданной с помощью функции [жетбаккупинстанце (JET_INSTANCE, String, баккупгрбит, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) .</span><span class="sxs-lookup"><span data-stu-id="6601f-105">It is designed to work with a backup created with the [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) function.</span></span> <span data-ttu-id="6601f-106">Это самая простая и наиболее функциональная функция Restore.</span><span class="sxs-lookup"><span data-stu-id="6601f-106">This is the simplest and most encapsulated restore function.</span></span>

<span data-ttu-id="6601f-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6601f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6601f-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6601f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6601f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6601f-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="6601f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6601f-110">Parameters</span></span>

  - <span data-ttu-id="6601f-111">экземпляр</span><span class="sxs-lookup"><span data-stu-id="6601f-111">instance</span></span>  
    <span data-ttu-id="6601f-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6601f-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="6601f-113">Используемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="6601f-113">The instance to use.</span></span> <span data-ttu-id="6601f-114">Экземпляр не должен инициализироваться.</span><span class="sxs-lookup"><span data-stu-id="6601f-114">The instance should not be initialized.</span></span> <span data-ttu-id="6601f-115">При восстановлении файлов экземпляр будет инициализирован.</span><span class="sxs-lookup"><span data-stu-id="6601f-115">Restoring the files will initialize the instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="6601f-116">source</span><span class="sxs-lookup"><span data-stu-id="6601f-116">source</span></span>  
    <span data-ttu-id="6601f-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6601f-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6601f-118">Расположение резервной копии.</span><span class="sxs-lookup"><span data-stu-id="6601f-118">Location of the backup.</span></span> <span data-ttu-id="6601f-119">Резервная копия должна быть создана с помощью [жетбаккупинстанце (JET_INSTANCE, String, баккупгрбит, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="6601f-119">The backup should have been created with [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="6601f-120">ресурс destination</span><span class="sxs-lookup"><span data-stu-id="6601f-120">destination</span></span>  
    <span data-ttu-id="6601f-121">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6601f-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6601f-122">Имя папки, в которую будут копироваться и восстанавливаться файлы базы данных из набора резервных копий.</span><span class="sxs-lookup"><span data-stu-id="6601f-122">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="6601f-123">Если задано значение null, файлы базы данных будут скопированы и восстановлены в исходном расположении.</span><span class="sxs-lookup"><span data-stu-id="6601f-123">If this is set to null, the database files will be copied and recovered to their original location.</span></span>

<!-- end list -->

  - <span data-ttu-id="6601f-124">статускаллбакк</span><span class="sxs-lookup"><span data-stu-id="6601f-124">statusCallback</span></span>  
    <span data-ttu-id="6601f-125">Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="6601f-125">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="6601f-126">Необязательный обратный вызов уведомления о состоянии.</span><span class="sxs-lookup"><span data-stu-id="6601f-126">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="6601f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6601f-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6601f-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="6601f-128">Reference</span></span>

[<span data-ttu-id="6601f-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="6601f-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6601f-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="6601f-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6601f-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6601f-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
