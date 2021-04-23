---
description: Дополнительные сведения о методе API. JetAttachDatabase2
title: API. JetAttachDatabase2, метод
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809227"
---
# <a name="apijetattachdatabase2-method"></a><span data-ttu-id="42249-103">API. JetAttachDatabase2, метод</span><span class="sxs-lookup"><span data-stu-id="42249-103">Api.JetAttachDatabase2 method</span></span>

<span data-ttu-id="42249-104">Присоединяет файл базы данных для использования с экземпляром базы данных.</span><span class="sxs-lookup"><span data-stu-id="42249-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="42249-105">Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью [жетопендатабасе (JET_SESID, String, String, JET_DBID, опендатабасегрбит)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="42249-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="42249-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42249-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42249-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42249-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42249-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42249-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="42249-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="42249-109">Parameters</span></span>

  - <span data-ttu-id="42249-110">сесид</span><span class="sxs-lookup"><span data-stu-id="42249-110">sesid</span></span>  
    <span data-ttu-id="42249-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="42249-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="42249-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="42249-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="42249-113">База данных</span><span class="sxs-lookup"><span data-stu-id="42249-113">database</span></span>  
    <span data-ttu-id="42249-114">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="42249-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="42249-115">База данных для присоединения.</span><span class="sxs-lookup"><span data-stu-id="42249-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="42249-116">макспажес</span><span class="sxs-lookup"><span data-stu-id="42249-116">maxPages</span></span>  
    <span data-ttu-id="42249-117">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="42249-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="42249-118">Максимальный размер базы данных в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="42249-118">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="42249-119">Передача значения 0 означает отсутствие принудительного применения максимального значения.</span><span class="sxs-lookup"><span data-stu-id="42249-119">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="42249-120">грбит</span><span class="sxs-lookup"><span data-stu-id="42249-120">grbit</span></span>  
    <span data-ttu-id="42249-121">Тип: [Microsoft. ISAM. ESENT. Interop. аттачдатабасегрбит](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="42249-121">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="42249-122">Параметры присоединения.</span><span class="sxs-lookup"><span data-stu-id="42249-122">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="42249-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42249-123">Return value</span></span>

<span data-ttu-id="42249-124">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="42249-124">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="42249-125">Код предупреждения ESENT.</span><span class="sxs-lookup"><span data-stu-id="42249-125">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="42249-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42249-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42249-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="42249-127">Reference</span></span>

[<span data-ttu-id="42249-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="42249-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="42249-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="42249-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="42249-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="42249-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
