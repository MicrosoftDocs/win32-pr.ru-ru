---
description: Дополнительные сведения о методе API. Жетсеттаблесекуентиал
title: API. Жетсеттаблесекуентиал, метод
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713015"
---
# <a name="apijetsettablesequential-method"></a><span data-ttu-id="49d46-103">API. Жетсеттаблесекуентиал, метод</span><span class="sxs-lookup"><span data-stu-id="49d46-103">Api.JetSetTableSequential method</span></span>

<span data-ttu-id="49d46-104">Уведомляет ядро СУБД о том, что приложение сканирует весь индекс, на котором расположен курсор.</span><span class="sxs-lookup"><span data-stu-id="49d46-104">Notifies the database engine that the application is scanning the entire index that the cursor is positioned on.</span></span> <span data-ttu-id="49d46-105">Следовательно, методы, используемые для доступа к данным индекса, будут настроены таким образом, чтобы сделать этот сценарий максимально быстрым.</span><span class="sxs-lookup"><span data-stu-id="49d46-105">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span> <span data-ttu-id="49d46-106">См. также [жетресеттаблесекуентиал (JET_SESID, JET_TABLEID, ресеттаблесекуентиалгрбит)](./api.jetresettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="49d46-106">Also see [JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span></span>

<span data-ttu-id="49d46-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49d46-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="49d46-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="49d46-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49d46-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49d46-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="49d46-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="49d46-110">Parameters</span></span>

  - <span data-ttu-id="49d46-111">сесид</span><span class="sxs-lookup"><span data-stu-id="49d46-111">sesid</span></span>  
    <span data-ttu-id="49d46-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49d46-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="49d46-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="49d46-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="49d46-114">TableID</span><span class="sxs-lookup"><span data-stu-id="49d46-114">tableid</span></span>  
    <span data-ttu-id="49d46-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49d46-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="49d46-116">Курсор, который будет обращаться к данным.</span><span class="sxs-lookup"><span data-stu-id="49d46-116">The cursor that will be accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="49d46-117">грбит</span><span class="sxs-lookup"><span data-stu-id="49d46-117">grbit</span></span>  
    <span data-ttu-id="49d46-118">Тип: [Microsoft. ISAM. ESENT. Interop. сеттаблесекуентиалгрбит](./settablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="49d46-118">Type: [Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="49d46-119">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="49d46-119">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="49d46-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49d46-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49d46-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="49d46-121">Reference</span></span>

[<span data-ttu-id="49d46-122">Класс API</span><span class="sxs-lookup"><span data-stu-id="49d46-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="49d46-123">Члены API</span><span class="sxs-lookup"><span data-stu-id="49d46-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="49d46-124">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="49d46-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
