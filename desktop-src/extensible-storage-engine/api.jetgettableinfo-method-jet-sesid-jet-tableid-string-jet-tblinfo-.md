---
description: 'Дополнительные сведения: метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, String, JET_TblInfo)'
title: Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, String, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, String, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100745
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01431c018e633a5851f8ca88eb2f2e6f0e9065a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713105"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-string-jet_tblinfo"></a><span data-ttu-id="acad3-103">Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, String, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="acad3-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, String, JET_TblInfo)</span></span>

<span data-ttu-id="acad3-104">Извлекает различные фрагменты информации о таблице в базе данных.</span><span class="sxs-lookup"><span data-stu-id="acad3-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="acad3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="acad3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="acad3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="acad3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="acad3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acad3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As String
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="acad3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="acad3-108">Parameters</span></span>

  - <span data-ttu-id="acad3-109">сесид</span><span class="sxs-lookup"><span data-stu-id="acad3-109">sesid</span></span>  
    <span data-ttu-id="acad3-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="acad3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="acad3-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="acad3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="acad3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="acad3-112">tableid</span></span>  
    <span data-ttu-id="acad3-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="acad3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="acad3-114">Таблица, сведения о которой необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="acad3-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="acad3-115">result</span><span class="sxs-lookup"><span data-stu-id="acad3-115">result</span></span>  
    <span data-ttu-id="acad3-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="acad3-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="acad3-117">Извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="acad3-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="acad3-118">инфолевел</span><span class="sxs-lookup"><span data-stu-id="acad3-118">infoLevel</span></span>  
    <span data-ttu-id="acad3-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="acad3-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="acad3-120">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="acad3-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="acad3-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="acad3-121">Remarks</span></span>

<span data-ttu-id="acad3-122">Эта перегрузка используется с [Name](./jet-tblinfo-enumeration.md) и [темплатетабленаме](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="acad3-122">This overload is used with [Name](./jet-tblinfo-enumeration.md) and [TemplateTableName](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="acad3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acad3-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="acad3-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="acad3-124">Reference</span></span>

[<span data-ttu-id="acad3-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="acad3-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="acad3-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="acad3-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="acad3-127">Перегрузка Жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="acad3-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="acad3-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="acad3-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
