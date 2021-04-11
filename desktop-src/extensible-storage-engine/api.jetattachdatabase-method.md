---
description: Дополнительные сведения о методе API. Жетаттачдатабасе
title: API. Жетаттачдатабасе, метод
TOCTitle: 'JetAttachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100652
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0447d4e6c5e8474c4d82340e35a23692096305bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143366"
---
# <a name="apijetattachdatabase-method"></a><span data-ttu-id="e6d91-103">API. Жетаттачдатабасе, метод</span><span class="sxs-lookup"><span data-stu-id="e6d91-103">Api.JetAttachDatabase method</span></span>

<span data-ttu-id="e6d91-104">Присоединяет файл базы данных для использования с экземпляром базы данных.</span><span class="sxs-lookup"><span data-stu-id="e6d91-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="e6d91-105">Чтобы использовать базу данных, ее потребуется впоследствии открыть с помощью [жетопендатабасе (JET_SESID, String, String, JET_DBID, опендатабасегрбит)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="e6d91-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="e6d91-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6d91-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6d91-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6d91-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d91-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6d91-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase(sesid, _
    database, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase(
    JET_SESID sesid,
    string database,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e6d91-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6d91-109">Parameters</span></span>

  - <span data-ttu-id="e6d91-110">сесид</span><span class="sxs-lookup"><span data-stu-id="e6d91-110">sesid</span></span>  
    <span data-ttu-id="e6d91-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e6d91-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e6d91-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="e6d91-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6d91-113">База данных</span><span class="sxs-lookup"><span data-stu-id="e6d91-113">database</span></span>  
    <span data-ttu-id="e6d91-114">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e6d91-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e6d91-115">База данных для присоединения.</span><span class="sxs-lookup"><span data-stu-id="e6d91-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6d91-116">грбит</span><span class="sxs-lookup"><span data-stu-id="e6d91-116">grbit</span></span>  
    <span data-ttu-id="e6d91-117">Тип: [Microsoft. ISAM. ESENT. Interop. аттачдатабасегрбит](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d91-117">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e6d91-118">Параметры присоединения.</span><span class="sxs-lookup"><span data-stu-id="e6d91-118">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e6d91-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6d91-119">Return value</span></span>

<span data-ttu-id="e6d91-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d91-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="e6d91-121">Код предупреждения ESENT.</span><span class="sxs-lookup"><span data-stu-id="e6d91-121">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6d91-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6d91-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6d91-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="e6d91-123">Reference</span></span>

[<span data-ttu-id="e6d91-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="e6d91-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e6d91-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="e6d91-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e6d91-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e6d91-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
