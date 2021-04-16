---
description: Дополнительные сведения о методе API. Жетжетаттачинфоинстанце
title: API. Жетжетаттачинфоинстанце, метод
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719323"
---
# <a name="apijetgetattachinfoinstance-method"></a><span data-ttu-id="337d2-103">API. Жетжетаттачинфоинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="337d2-103">Api.JetGetAttachInfoInstance method</span></span>

<span data-ttu-id="337d2-104">Используется во время резервного копирования, инициированного [жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)](./api.jetbeginexternalbackupinstance-method.md) , для запроса экземпляров имен файлов базы данных, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="337d2-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="337d2-105">Будут рассматриваться только те базы данных, которые в данный момент подключены к экземпляру с помощью [жетаттачдатабасе (JET_SESID, String, аттачдатабасегрбит)](./api.jetattachdatabase-method.md) .</span><span class="sxs-lookup"><span data-stu-id="337d2-105">Only databases that are currently attached to the instance using [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will be considered.</span></span> <span data-ttu-id="337d2-106">Эти файлы впоследствии можно открыть с помощью [жетопенфилеинстанце (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) и считывать с помощью [жетреадфилеинстанце (JET_INSTANCE, JET_HANDLE, \[ \] Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="337d2-106">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="337d2-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="337d2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="337d2-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="337d2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="337d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="337d2-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="337d2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="337d2-110">Parameters</span></span>

  - <span data-ttu-id="337d2-111">экземпляр</span><span class="sxs-lookup"><span data-stu-id="337d2-111">instance</span></span>  
    <span data-ttu-id="337d2-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="337d2-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="337d2-113">Экземпляр, для которого необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="337d2-113">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="337d2-114">files</span><span class="sxs-lookup"><span data-stu-id="337d2-114">files</span></span>  
    <span data-ttu-id="337d2-115">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="337d2-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="337d2-116">Возвращает список строк, заканчивающихся нулем, описывающих набор файлов базы данных, который должен быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="337d2-116">Returns a list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="337d2-117">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="337d2-117">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="337d2-118">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="337d2-118">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="337d2-119">maxChars</span><span class="sxs-lookup"><span data-stu-id="337d2-119">maxChars</span></span>  
    <span data-ttu-id="337d2-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="337d2-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="337d2-121">Максимальное число извлекаемых символов.</span><span class="sxs-lookup"><span data-stu-id="337d2-121">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="337d2-122">актуалчарс</span><span class="sxs-lookup"><span data-stu-id="337d2-122">actualChars</span></span>  
    <span data-ttu-id="337d2-123">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="337d2-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="337d2-124">Фактический размер списка файлов.</span><span class="sxs-lookup"><span data-stu-id="337d2-124">Actual size of the file list.</span></span> <span data-ttu-id="337d2-125">Если это значение больше maxChars, список был обрезан.</span><span class="sxs-lookup"><span data-stu-id="337d2-125">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="337d2-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="337d2-126">Remarks</span></span>

<span data-ttu-id="337d2-127">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="337d2-127">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="337d2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="337d2-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="337d2-129">Справочник</span><span class="sxs-lookup"><span data-stu-id="337d2-129">Reference</span></span>

[<span data-ttu-id="337d2-130">Класс API</span><span class="sxs-lookup"><span data-stu-id="337d2-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="337d2-131">Члены API</span><span class="sxs-lookup"><span data-stu-id="337d2-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="337d2-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="337d2-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
