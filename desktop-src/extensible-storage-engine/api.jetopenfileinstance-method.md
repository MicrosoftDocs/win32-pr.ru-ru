---
description: Дополнительные сведения о методе API. Жетопенфилеинстанце
title: API. Жетопенфилеинстанце, метод
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712925"
---
# <a name="apijetopenfileinstance-method"></a><span data-ttu-id="6b939-103">API. Жетопенфилеинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="6b939-103">Api.JetOpenFileInstance method</span></span>

<span data-ttu-id="6b939-104">Открывает присоединенную базу данных, файл исправления базы данных или файл журнала транзакций активного экземпляра с целью выполнения потоковой архивации нечеткого резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6b939-104">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="6b939-105">Затем данные из этих файлов можно считать с помощью возвращенного маркера с помощью Жетреадфилеинстанце.</span><span class="sxs-lookup"><span data-stu-id="6b939-105">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="6b939-106">Возвращаемый обработчик должен быть закрыт с помощью Жетклосефилеинстанце.</span><span class="sxs-lookup"><span data-stu-id="6b939-106">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="6b939-107">Внешнее резервное копирование экземпляра должно быть ранее инициировано с помощью Жетбегинекстерналбаккупинстанце.</span><span class="sxs-lookup"><span data-stu-id="6b939-107">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span>

<span data-ttu-id="6b939-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6b939-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6b939-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6b939-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b939-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b939-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a><span data-ttu-id="6b939-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b939-111">Parameters</span></span>

  - <span data-ttu-id="6b939-112">экземпляр</span><span class="sxs-lookup"><span data-stu-id="6b939-112">instance</span></span>  
    <span data-ttu-id="6b939-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6b939-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="6b939-114">Используемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="6b939-114">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b939-115">файл</span><span class="sxs-lookup"><span data-stu-id="6b939-115">file</span></span>  
    <span data-ttu-id="6b939-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6b939-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6b939-117">Открываемый файл.</span><span class="sxs-lookup"><span data-stu-id="6b939-117">The file to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b939-118">handle</span><span class="sxs-lookup"><span data-stu-id="6b939-118">handle</span></span>  
    <span data-ttu-id="6b939-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6b939-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="6b939-120">Возвращает маркер файла.</span><span class="sxs-lookup"><span data-stu-id="6b939-120">Returns a handle to the file.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b939-121">филесизелов</span><span class="sxs-lookup"><span data-stu-id="6b939-121">fileSizeLow</span></span>  
    <span data-ttu-id="6b939-122">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="6b939-122">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="6b939-123">Возвращает минимальный значащий 32 бит размера файла.</span><span class="sxs-lookup"><span data-stu-id="6b939-123">Returns the least significant 32 bits of the file size.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b939-124">филесизехигх</span><span class="sxs-lookup"><span data-stu-id="6b939-124">fileSizeHigh</span></span>  
    <span data-ttu-id="6b939-125">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="6b939-125">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="6b939-126">Возвращает наиболее значимый 32 бит размера файла.</span><span class="sxs-lookup"><span data-stu-id="6b939-126">Returns the most significant 32 bits of the file size.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b939-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b939-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6b939-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="6b939-128">Reference</span></span>

[<span data-ttu-id="6b939-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="6b939-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6b939-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="6b939-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6b939-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6b939-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
