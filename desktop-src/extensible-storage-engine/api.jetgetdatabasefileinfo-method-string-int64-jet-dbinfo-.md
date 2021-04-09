---
description: 'Дополнительные сведения: метод API. Жетжетдатабасефилеинфо (String, Int64, JET_DbInfo)'
title: Метод API. Жетжетдатабасефилеинфо (String, Int64, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc036a1c1eceedd39fd265bcf85a2dbaf779a432
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144326"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a><span data-ttu-id="71562-103">Метод API. Жетжетдатабасефилеинфо (String, Int64, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="71562-103">Api.JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)</span></span>

<span data-ttu-id="71562-104">Извлекает определенные сведения о заданной базе данных.</span><span class="sxs-lookup"><span data-stu-id="71562-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="71562-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71562-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71562-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71562-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71562-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71562-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="71562-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="71562-108">Parameters</span></span>

  - <span data-ttu-id="71562-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="71562-109">databaseName</span></span>  
    <span data-ttu-id="71562-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="71562-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="71562-111">Имя файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="71562-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="71562-112">значение</span><span class="sxs-lookup"><span data-stu-id="71562-112">value</span></span>  
    <span data-ttu-id="71562-113">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="71562-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="71562-114">Получаемое значение.</span><span class="sxs-lookup"><span data-stu-id="71562-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="71562-115">инфолевел</span><span class="sxs-lookup"><span data-stu-id="71562-115">infoLevel</span></span>  
    <span data-ttu-id="71562-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="71562-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="71562-117">Конкретные извлекаемые данные.</span><span class="sxs-lookup"><span data-stu-id="71562-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="71562-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71562-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71562-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="71562-119">Reference</span></span>

[<span data-ttu-id="71562-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="71562-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="71562-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="71562-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="71562-122">Перегрузка Жетжетдатабасефилеинфо</span><span class="sxs-lookup"><span data-stu-id="71562-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="71562-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="71562-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
