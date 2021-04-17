---
description: Дополнительные сведения о методе API. Жетсетдатабасесизе
title: API. Жетсетдатабасесизе, метод
TOCTitle: 'JetSetDatabaseSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetdatabasesize(v=EXCHG.10)
ms:contentKeyID: 55100807
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c90ba5ef2ebc96cbe6d50fa6c0888db9a09a0a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674101"
---
# <a name="apijetsetdatabasesize-method"></a><span data-ttu-id="1fa5b-103">API. Жетсетдатабасесизе, метод</span><span class="sxs-lookup"><span data-stu-id="1fa5b-103">Api.JetSetDatabaseSize method</span></span>

<span data-ttu-id="1fa5b-104">Задает размер неоткрытого файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="1fa5b-104">Sets the size of an unopened database file.</span></span>

<span data-ttu-id="1fa5b-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fa5b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1fa5b-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1fa5b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa5b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fa5b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetDatabaseSize ( _
    sesid As JET_SESID, _
    database As String, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetSetDatabaseSize(sesid, database, _
    desiredPages, actualPages)
```

``` csharp
public static void JetSetDatabaseSize(
    JET_SESID sesid,
    string database,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="1fa5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fa5b-108">Parameters</span></span>

  - <span data-ttu-id="1fa5b-109">сесид</span><span class="sxs-lookup"><span data-stu-id="1fa5b-109">sesid</span></span>  
    <span data-ttu-id="1fa5b-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1fa5b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1fa5b-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="1fa5b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fa5b-112">База данных</span><span class="sxs-lookup"><span data-stu-id="1fa5b-112">database</span></span>  
    <span data-ttu-id="1fa5b-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1fa5b-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1fa5b-114">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="1fa5b-114">The name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fa5b-115">десиредпажес</span><span class="sxs-lookup"><span data-stu-id="1fa5b-115">desiredPages</span></span>  
    <span data-ttu-id="1fa5b-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1fa5b-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1fa5b-117">Требуемый размер базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="1fa5b-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="1fa5b-118">актуалпажес</span><span class="sxs-lookup"><span data-stu-id="1fa5b-118">actualPages</span></span>  
    <span data-ttu-id="1fa5b-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1fa5b-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1fa5b-120">Размер базы данных на страницах после вызова.</span><span class="sxs-lookup"><span data-stu-id="1fa5b-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fa5b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fa5b-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fa5b-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="1fa5b-122">Reference</span></span>

[<span data-ttu-id="1fa5b-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="1fa5b-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1fa5b-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="1fa5b-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1fa5b-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1fa5b-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
