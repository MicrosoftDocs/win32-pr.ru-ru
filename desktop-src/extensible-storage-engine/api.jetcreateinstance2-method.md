---
description: Дополнительные сведения о методе API. JetCreateInstance2
title: API. JetCreateInstance2, метод
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d21974d5c3bd5ca6dfbab2ac493d19b202ca6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701425"
---
# <a name="apijetcreateinstance2-method"></a><span data-ttu-id="a6dcf-103">API. JetCreateInstance2, метод</span><span class="sxs-lookup"><span data-stu-id="a6dcf-103">Api.JetCreateInstance2 method</span></span>

<span data-ttu-id="a6dcf-104">Выделение нового экземпляра ядра СУБД для использования в одном процессе с указанным отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="a6dcf-104">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="a6dcf-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6dcf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a6dcf-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a6dcf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6dcf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6dcf-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a6dcf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6dcf-108">Parameters</span></span>

  - <span data-ttu-id="a6dcf-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="a6dcf-109">instance</span></span>  
    <span data-ttu-id="a6dcf-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a6dcf-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="a6dcf-111">Возвращает вновь созданный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a6dcf-111">Returns the newly create instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6dcf-112">name</span><span class="sxs-lookup"><span data-stu-id="a6dcf-112">name</span></span>  
    <span data-ttu-id="a6dcf-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a6dcf-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a6dcf-114">Задает уникальный идентификатор строки для создаваемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a6dcf-114">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="a6dcf-115">Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="a6dcf-115">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6dcf-116">displayName</span><span class="sxs-lookup"><span data-stu-id="a6dcf-116">displayName</span></span>  
    <span data-ttu-id="a6dcf-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a6dcf-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a6dcf-118">Отображаемое имя создаваемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a6dcf-118">A display name for the instance to be created.</span></span> <span data-ttu-id="a6dcf-119">Он будет использоваться в записях журнала событий.</span><span class="sxs-lookup"><span data-stu-id="a6dcf-119">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6dcf-120">грбит</span><span class="sxs-lookup"><span data-stu-id="a6dcf-120">grbit</span></span>  
    <span data-ttu-id="a6dcf-121">Тип: [Microsoft. ISAM. ESENT. Interop. креатеинстанцегрбит](./createinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a6dcf-121">Type: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a6dcf-122">Параметры создания.</span><span class="sxs-lookup"><span data-stu-id="a6dcf-122">Creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6dcf-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6dcf-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6dcf-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="a6dcf-124">Reference</span></span>

[<span data-ttu-id="a6dcf-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="a6dcf-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a6dcf-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="a6dcf-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a6dcf-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a6dcf-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
