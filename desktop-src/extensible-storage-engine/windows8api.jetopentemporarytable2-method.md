---
description: 'Дополнительные сведения о методе: Windows8Api. JetOpenTemporaryTable2'
title: Windows8Api. JetOpenTemporaryTable2, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- DllExport
api_location:
- Microsoft.Isam.Esent.Interop.dll
- esent.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb01792608ec542918f4bd8ff6ec06ef27091bb1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691733"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="d4b25-103">Windows8Api. JetOpenTemporaryTable2, метод</span><span class="sxs-lookup"><span data-stu-id="d4b25-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="d4b25-104">Создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="d4b25-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="d4b25-105">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="d4b25-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="d4b25-106">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="d4b25-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="d4b25-107">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="d4b25-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="d4b25-108">См. также [жетопентемптабле (JET_SESID, \[ \] , Int32, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "API. JetOpenTempTable2", [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="d4b25-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="d4b25-109">[Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="d4b25-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="d4b25-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d4b25-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="d4b25-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d4b25-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b25-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4b25-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="d4b25-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4b25-113">Parameters</span></span>

  - <span data-ttu-id="d4b25-114">сесид</span><span class="sxs-lookup"><span data-stu-id="d4b25-114">sesid</span></span>  
    <span data-ttu-id="d4b25-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d4b25-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d4b25-116">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="d4b25-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d4b25-117">темпораритабле</span><span class="sxs-lookup"><span data-stu-id="d4b25-117">temporarytable</span></span>  
    <span data-ttu-id="d4b25-118">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="d4b25-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="d4b25-119">Описание временной таблицы, создаваемой на входе.</span><span class="sxs-lookup"><span data-stu-id="d4b25-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="d4b25-120">После успешного вызова структура содержит описатель для временной таблицы и идентификаторов столбцов.</span><span class="sxs-lookup"><span data-stu-id="d4b25-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="d4b25-121">Используйте [жетклосетабле (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) , чтобы освободить временную таблицу по завершении.</span><span class="sxs-lookup"><span data-stu-id="d4b25-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4b25-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4b25-122">Remarks</span></span>

<span data-ttu-id="d4b25-123">Используйте [жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) для более ранних версий ESENT.</span><span class="sxs-lookup"><span data-stu-id="d4b25-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4b25-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4b25-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d4b25-125">Ссылка</span><span class="sxs-lookup"><span data-stu-id="d4b25-125">Reference</span></span>

[<span data-ttu-id="d4b25-126">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="d4b25-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="d4b25-127">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="d4b25-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="d4b25-128">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="d4b25-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
