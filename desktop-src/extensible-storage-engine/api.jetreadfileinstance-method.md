---
description: Дополнительные сведения о методе API. Жетреадфилеинстанце
title: API. Жетреадфилеинстанце, метод
TOCTitle: 'JetReadFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetreadfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100781
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80eaf61fd9cd07fce80d32fddf7056f6bff683c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703159"
---
# <a name="apijetreadfileinstance-method"></a><span data-ttu-id="312b2-103">API. Жетреадфилеинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="312b2-103">Api.JetReadFileInstance method</span></span>

<span data-ttu-id="312b2-104">Извлекает содержимое файла, открытого с помощью [жетопенфилеинстанце (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="312b2-104">Retrieves the contents of a file opened with [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span></span>

<span data-ttu-id="312b2-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="312b2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="312b2-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="312b2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="312b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="312b2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetReadFileInstance ( _
    instance As JET_INSTANCE, _
    file As JET_HANDLE, _
    buffer As Byte(), _
    bufferSize As Integer, _
    <OutAttribute> ByRef bytesRead As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As JET_HANDLE
Dim buffer As Byte()
Dim bufferSize As Integer
Dim bytesRead As IntegerApi.JetReadFileInstance(instance, _
    file, buffer, bufferSize, bytesRead)
```

``` csharp
public static void JetReadFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE file,
    byte[] buffer,
    int bufferSize,
    out int bytesRead
)
```

#### <a name="parameters"></a><span data-ttu-id="312b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="312b2-108">Parameters</span></span>

  - <span data-ttu-id="312b2-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="312b2-109">instance</span></span>  
    <span data-ttu-id="312b2-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="312b2-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="312b2-111">Используемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="312b2-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="312b2-112">файл</span><span class="sxs-lookup"><span data-stu-id="312b2-112">file</span></span>  
    <span data-ttu-id="312b2-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="312b2-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="312b2-114">Файл, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="312b2-114">The file to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="312b2-115">buffer</span><span class="sxs-lookup"><span data-stu-id="312b2-115">buffer</span></span>  
    <span data-ttu-id="312b2-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="312b2-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="312b2-117">Буфер, в который производится чтение.</span><span class="sxs-lookup"><span data-stu-id="312b2-117">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="312b2-118">bufferSize</span><span class="sxs-lookup"><span data-stu-id="312b2-118">bufferSize</span></span>  
    <span data-ttu-id="312b2-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="312b2-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="312b2-120">Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="312b2-120">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="312b2-121">битесреад</span><span class="sxs-lookup"><span data-stu-id="312b2-121">bytesRead</span></span>  
    <span data-ttu-id="312b2-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="312b2-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="312b2-123">Возвращает объем данных, считанных в буфер.</span><span class="sxs-lookup"><span data-stu-id="312b2-123">Returns the amount of data read into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="312b2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="312b2-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="312b2-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="312b2-125">Reference</span></span>

[<span data-ttu-id="312b2-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="312b2-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="312b2-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="312b2-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="312b2-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="312b2-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
