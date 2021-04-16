---
description: Дополнительные сведения о методе API. Жетфрибуффер
title: API. Жетфрибуффер, метод
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719324"
---
# <a name="apijetfreebuffer-method"></a><span data-ttu-id="314d4-103">API. Жетфрибуффер, метод</span><span class="sxs-lookup"><span data-stu-id="314d4-103">Api.JetFreeBuffer method</span></span>

<span data-ttu-id="314d4-104">Освобождает память, выделенную при вызове ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="314d4-104">Frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="314d4-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="314d4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="314d4-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="314d4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="314d4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="314d4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a><span data-ttu-id="314d4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="314d4-108">Parameters</span></span>

  - <span data-ttu-id="314d4-109">buffer</span><span class="sxs-lookup"><span data-stu-id="314d4-109">buffer</span></span>  
    <span data-ttu-id="314d4-110">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="314d4-110">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="314d4-111">Буфер, выделенный при вызове ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="314d4-111">The buffer allocated by a call to the database engine.</span></span> <span data-ttu-id="314d4-112">[Ноль](/dotnet/api/system.intptr.zero) является допустимым и будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="314d4-112">[Zero](/dotnet/api/system.intptr.zero) is acceptable, and will be ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="314d4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="314d4-113">Remarks</span></span>

<span data-ttu-id="314d4-114">Этот метод является внутренним, поскольку мы никогда не предоставляем память, выделенную функцией ESENT вызывающим объектам.</span><span class="sxs-lookup"><span data-stu-id="314d4-114">This method is internal because we never expose the memory allocated by ESENT to our callers.</span></span>

## <a name="see-also"></a><span data-ttu-id="314d4-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="314d4-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="314d4-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="314d4-116">Reference</span></span>

[<span data-ttu-id="314d4-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="314d4-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="314d4-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="314d4-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="314d4-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="314d4-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
