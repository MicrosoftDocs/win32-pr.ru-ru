---
description: Дополнительные сведения о методе API. Жетжеттрункателогинфоинстанце
title: API. Жетжеттрункателогинфоинстанце, метод
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272735"
---
# <a name="apijetgettruncateloginfoinstance-method"></a><span data-ttu-id="4a9f2-103">API. Жетжеттрункателогинфоинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="4a9f2-103">Api.JetGetTruncateLogInfoInstance method</span></span>

<span data-ttu-id="4a9f2-104">Используется во время резервного копирования, инициированного [жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)](./api.jetbeginexternalbackupinstance-method.md) , чтобы запросить у экземпляра имена файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="4a9f2-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a9f2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a9f2-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a9f2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9f2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a9f2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="4a9f2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a9f2-108">Parameters</span></span>

  - <span data-ttu-id="4a9f2-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="4a9f2-109">instance</span></span>  
    <span data-ttu-id="4a9f2-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a9f2-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="4a9f2-111">Экземпляр, для которого необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-111">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a9f2-112">files</span><span class="sxs-lookup"><span data-stu-id="4a9f2-112">files</span></span>  
    <span data-ttu-id="4a9f2-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4a9f2-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4a9f2-114">Возвращает список строк, заканчивающихся нулем, описывающих набор файлов журнала базы данных, которые можно безопасно удалить после завершения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-114">Returns a list of null terminated strings describing the set of database log files that can be safely deleted after the backup completes.</span></span> <span data-ttu-id="4a9f2-115">Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-115">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="4a9f2-116">Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-116">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a9f2-117">maxChars</span><span class="sxs-lookup"><span data-stu-id="4a9f2-117">maxChars</span></span>  
    <span data-ttu-id="4a9f2-118">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4a9f2-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4a9f2-119">Максимальное число извлекаемых символов.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-119">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a9f2-120">актуалчарс</span><span class="sxs-lookup"><span data-stu-id="4a9f2-120">actualChars</span></span>  
    <span data-ttu-id="4a9f2-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4a9f2-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4a9f2-122">Фактический размер списка файлов.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-122">Actual size of the file list.</span></span> <span data-ttu-id="4a9f2-123">Если это значение больше maxChars, список был обрезан.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-123">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a9f2-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a9f2-124">Remarks</span></span>

<span data-ttu-id="4a9f2-125">Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="4a9f2-125">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a9f2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a9f2-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a9f2-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="4a9f2-127">Reference</span></span>

[<span data-ttu-id="4a9f2-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="4a9f2-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4a9f2-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="4a9f2-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4a9f2-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a9f2-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
