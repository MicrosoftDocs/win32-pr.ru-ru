---
description: Дополнительные сведения о методе API. Жетжетлогинфоинстанце
title: API. Жетжетлогинфоинстанце, метод
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85e252b74c47d3274fc83af59e3fb571906219fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650502"
---
# <a name="apijetgetloginfoinstance-method"></a><span data-ttu-id="3353e-103">API. Жетжетлогинфоинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="3353e-103">Api.JetGetLogInfoInstance method</span></span>

<span data-ttu-id="3353e-104">Используется во время резервного копирования, инициированного [жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)](./api.jetbeginexternalbackupinstance-method.md) , чтобы запрашивать имена файлов исправления базы данных и журналов, которые должны стать частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3353e-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database patch files and logfiles that should become part of the backup file set.</span></span> <span data-ttu-id="3353e-105">Эти файлы впоследствии можно открыть с помощью [жетопенфилеинстанце (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) и считывать с помощью [жетреадфилеинстанце (JET_INSTANCE, JET_HANDLE, \[ \] Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="3353e-105">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="3353e-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3353e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3353e-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3353e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3353e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3353e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="3353e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3353e-109">Parameters</span></span>

  - <span data-ttu-id="3353e-110">экземпляр</span><span class="sxs-lookup"><span data-stu-id="3353e-110">instance</span></span>  
    <span data-ttu-id="3353e-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3353e-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="3353e-112">Экземпляр, для которого необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="3353e-112">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="3353e-113">files</span><span class="sxs-lookup"><span data-stu-id="3353e-113">files</span></span>  
    <span data-ttu-id="3353e-114">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3353e-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3353e-115">Возвращает список строк, заканчивающихся нулем, описывающих набор файлов исправления базы данных и файлов журналов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3353e-115">Returns a list of null terminated strings describing the set of database patch files and log files that should be a part of the backup file set.</span></span> <span data-ttu-id="3353e-116">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="3353e-116">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="3353e-117">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="3353e-117">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="3353e-118">maxChars</span><span class="sxs-lookup"><span data-stu-id="3353e-118">maxChars</span></span>  
    <span data-ttu-id="3353e-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3353e-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3353e-120">Максимальное число извлекаемых символов.</span><span class="sxs-lookup"><span data-stu-id="3353e-120">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="3353e-121">актуалчарс</span><span class="sxs-lookup"><span data-stu-id="3353e-121">actualChars</span></span>  
    <span data-ttu-id="3353e-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3353e-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3353e-123">Фактический размер списка файлов.</span><span class="sxs-lookup"><span data-stu-id="3353e-123">Actual size of the file list.</span></span> <span data-ttu-id="3353e-124">Если это значение больше maxChars, список был обрезан.</span><span class="sxs-lookup"><span data-stu-id="3353e-124">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="3353e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3353e-125">Remarks</span></span>

<span data-ttu-id="3353e-126">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3353e-126">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="3353e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3353e-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3353e-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="3353e-128">Reference</span></span>

[<span data-ttu-id="3353e-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="3353e-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3353e-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="3353e-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3353e-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3353e-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
