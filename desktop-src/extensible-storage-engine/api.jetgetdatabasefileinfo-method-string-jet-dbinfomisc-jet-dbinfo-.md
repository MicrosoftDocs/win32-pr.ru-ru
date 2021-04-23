---
description: 'Дополнительные сведения: метод API. Жетжетдатабасефилеинфо (String, JET_DBINFOMISC, JET_DbInfo)'
title: Метод API. Жетжетдатабасефилеинфо (String, JET_DBINFOMISC, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,Microsoft.Isam.Esent.Interop.JET_DBINFOMISC@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d72711314312c843d9e456a5194cb6133b4f491f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144323"
---
# <a name="apijetgetdatabasefileinfo-method-string-jet_dbinfomisc-jet_dbinfo"></a><span data-ttu-id="01616-103">Метод API. Жетжетдатабасефилеинфо (String, JET_DBINFOMISC, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="01616-103">Api.JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)</span></span>

<span data-ttu-id="01616-104">Извлекает определенные сведения о заданной базе данных.</span><span class="sxs-lookup"><span data-stu-id="01616-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="01616-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01616-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01616-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01616-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01616-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01616-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef dbinfomisc As JET_DBINFOMISC, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim dbinfomisc As JET_DBINFOMISC
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    dbinfomisc, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out JET_DBINFOMISC dbinfomisc,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="01616-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01616-108">Parameters</span></span>

  - <span data-ttu-id="01616-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="01616-109">databaseName</span></span>  
    <span data-ttu-id="01616-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="01616-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="01616-111">Имя файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="01616-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="01616-112">дбинфомиск</span><span class="sxs-lookup"><span data-stu-id="01616-112">dbinfomisc</span></span>  
    <span data-ttu-id="01616-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span><span class="sxs-lookup"><span data-stu-id="01616-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span></span>  
    
    <span data-ttu-id="01616-114">Получаемое значение.</span><span class="sxs-lookup"><span data-stu-id="01616-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="01616-115">инфолевел</span><span class="sxs-lookup"><span data-stu-id="01616-115">infoLevel</span></span>  
    <span data-ttu-id="01616-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="01616-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="01616-117">Конкретные извлекаемые данные.</span><span class="sxs-lookup"><span data-stu-id="01616-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="01616-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01616-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01616-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="01616-119">Reference</span></span>

[<span data-ttu-id="01616-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="01616-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="01616-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="01616-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="01616-122">Перегрузка Жетжетдатабасефилеинфо</span><span class="sxs-lookup"><span data-stu-id="01616-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="01616-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="01616-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
