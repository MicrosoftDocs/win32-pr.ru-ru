---
description: 'Дополнительные сведения о методе: Вистаапи. Жетопентемпораритабле'
title: Вистаапи. Жетопентемпораритабле, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711577"
---
# <a name="vistaapijetopentemporarytable-method"></a><span data-ttu-id="5bd0c-103">Вистаапи. Жетопентемпораритабле, метод</span><span class="sxs-lookup"><span data-stu-id="5bd0c-103">VistaApi.JetOpenTemporaryTable method</span></span>

<span data-ttu-id="5bd0c-104">Создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="5bd0c-105">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="5bd0c-106">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="5bd0c-107">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="5bd0c-108">См. также [жетопентемптабле (JET_SESID, \[ \] , Int32, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="5bd0c-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span>

<span data-ttu-id="5bd0c-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5bd0c-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="5bd0c-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5bd0c-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd0c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bd0c-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="5bd0c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bd0c-112">Parameters</span></span>

  - <span data-ttu-id="5bd0c-113">сесид</span><span class="sxs-lookup"><span data-stu-id="5bd0c-113">sesid</span></span>  
    <span data-ttu-id="5bd0c-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5bd0c-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5bd0c-115">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bd0c-116">темпораритабле</span><span class="sxs-lookup"><span data-stu-id="5bd0c-116">temporarytable</span></span>  
    <span data-ttu-id="5bd0c-117">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="5bd0c-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="5bd0c-118">Описание временной таблицы, создаваемой на входе.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-118">Description of the temporary table to create on input.</span></span> <span data-ttu-id="5bd0c-119">После успешного вызова структура содержит описатель для временной таблицы и идентификаторов столбцов.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-119">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="5bd0c-120">Используйте [жетклосетабле (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) , чтобы освободить временную таблицу по завершении.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-120">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd0c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bd0c-121">Remarks</span></span>

<span data-ttu-id="5bd0c-122">Впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-122">Introduced in Windows Vista.</span></span> <span data-ttu-id="5bd0c-123">Используйте [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) для более ранних версий ESENT.</span><span class="sxs-lookup"><span data-stu-id="5bd0c-123">Use [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bd0c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bd0c-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5bd0c-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="5bd0c-125">Reference</span></span>

[<span data-ttu-id="5bd0c-126">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="5bd0c-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="5bd0c-127">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="5bd0c-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="5bd0c-128">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="5bd0c-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
