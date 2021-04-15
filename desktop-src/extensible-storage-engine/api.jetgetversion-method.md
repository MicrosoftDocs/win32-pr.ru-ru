---
description: Дополнительные сведения о методе API. Жетжетверсион
title: API. Жетжетверсион, метод
TOCTitle: 'JetGetVersion method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetVersion(Microsoft.Isam.Esent.Interop.JET_SESID,System.UInt32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetversion(v=EXCHG.10)
ms:contentKeyID: 55100744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8860b21ec2b5db3841b866aa9c1c2cc7cff300aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543463"
---
# <a name="apijetgetversion-method"></a><span data-ttu-id="999c0-103">API. Жетжетверсион, метод</span><span class="sxs-lookup"><span data-stu-id="999c0-103">Api.JetGetVersion method</span></span>

<span data-ttu-id="999c0-104">Извлекает версию ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="999c0-104">Retrieves the version of the database engine.</span></span>

<span data-ttu-id="999c0-105">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="999c0-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="999c0-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="999c0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="999c0-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="999c0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="999c0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="999c0-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetVersion ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef version As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim version As UIntegerApi.JetGetVersion(sesid, version)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetVersion(
    JET_SESID sesid,
    out uint version
)
```

#### <a name="parameters"></a><span data-ttu-id="999c0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="999c0-109">Parameters</span></span>

  - <span data-ttu-id="999c0-110">сесид</span><span class="sxs-lookup"><span data-stu-id="999c0-110">sesid</span></span>  
    <span data-ttu-id="999c0-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="999c0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="999c0-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="999c0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="999c0-113">version</span><span class="sxs-lookup"><span data-stu-id="999c0-113">version</span></span>  
    <span data-ttu-id="999c0-114">Тип: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="999c0-114">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="999c0-115">Возвращает номер версии ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="999c0-115">Returns the version number of the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="999c0-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="999c0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="999c0-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="999c0-117">Reference</span></span>

[<span data-ttu-id="999c0-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="999c0-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="999c0-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="999c0-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="999c0-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="999c0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
