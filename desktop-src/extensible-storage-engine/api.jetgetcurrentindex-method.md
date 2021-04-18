---
description: Дополнительные сведения о методе API. Жетжеткуррентиндекс
title: API. Жетжеткуррентиндекс, метод
TOCTitle: 'JetGetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bacc6973b1a105e128533a1116abdeb4c6cfafa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710950"
---
# <a name="apijetgetcurrentindex-method"></a><span data-ttu-id="d106b-103">API. Жетжеткуррентиндекс, метод</span><span class="sxs-lookup"><span data-stu-id="d106b-103">Api.JetGetCurrentIndex method</span></span>

<span data-ttu-id="d106b-104">Ддетерминес имя текущего индекса данного курсора.</span><span class="sxs-lookup"><span data-stu-id="d106b-104">Ddetermines the name of the current index of a given cursor.</span></span> <span data-ttu-id="d106b-105">Это имя также используется для повторного выбора этого индекса в качестве текущего индекса с помощью [жетсеткуррентиндекс (JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span><span class="sxs-lookup"><span data-stu-id="d106b-105">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span></span> <span data-ttu-id="d106b-106">Его также можно использовать для обнаружения свойств этого индекса с помощью Жетжеттаблеиндексинфо.</span><span class="sxs-lookup"><span data-stu-id="d106b-106">It can also be used to discover the properties of that index using JetGetTableIndexInfo.</span></span>

<span data-ttu-id="d106b-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d106b-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d106b-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d106b-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d106b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d106b-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef indexName As String, _
    maxNameLength As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim maxNameLength As IntegerApi.JetGetCurrentIndex(sesid, tableid, _
    indexName, maxNameLength)
```

``` csharp
public static void JetGetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string indexName,
    int maxNameLength
)
```

#### <a name="parameters"></a><span data-ttu-id="d106b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d106b-110">Parameters</span></span>

  - <span data-ttu-id="d106b-111">сесид</span><span class="sxs-lookup"><span data-stu-id="d106b-111">sesid</span></span>  
    <span data-ttu-id="d106b-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d106b-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d106b-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="d106b-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d106b-114">TableID</span><span class="sxs-lookup"><span data-stu-id="d106b-114">tableid</span></span>  
    <span data-ttu-id="d106b-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d106b-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d106b-116">Курсор, для которого необходимо получить имя индекса.</span><span class="sxs-lookup"><span data-stu-id="d106b-116">The cursor to get the index name for.</span></span>

<!-- end list -->

  - <span data-ttu-id="d106b-117">indexName</span><span class="sxs-lookup"><span data-stu-id="d106b-117">indexName</span></span>  
    <span data-ttu-id="d106b-118">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d106b-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d106b-119">Возвращает имя индекса.</span><span class="sxs-lookup"><span data-stu-id="d106b-119">Returns the name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="d106b-120">maxNameLength</span><span class="sxs-lookup"><span data-stu-id="d106b-120">maxNameLength</span></span>  
    <span data-ttu-id="d106b-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d106b-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d106b-122">Максимальная длина имени индекса.</span><span class="sxs-lookup"><span data-stu-id="d106b-122">The maximum length of the index name.</span></span> <span data-ttu-id="d106b-123">Длина имен индексов не превышает [намемост](./systemparameters.namemost-field.md) символов.</span><span class="sxs-lookup"><span data-stu-id="d106b-123">Index names are no more than [NameMost](./systemparameters.namemost-field.md) characters.</span></span>

## <a name="see-also"></a><span data-ttu-id="d106b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d106b-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d106b-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="d106b-125">Reference</span></span>

[<span data-ttu-id="d106b-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="d106b-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d106b-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="d106b-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d106b-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d106b-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
