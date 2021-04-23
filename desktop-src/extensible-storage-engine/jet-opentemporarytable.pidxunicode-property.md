---
description: 'Дополнительные сведения о свойстве: JET_OPENTEMPORARYTABLE. пидксуникоде'
title: Свойство JET_OPENTEMPORARYTABLE. пидксуникоде (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703103"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a><span data-ttu-id="a00e5-103">Свойство JET_OPENTEMPORARYTABLE. пидксуникоде</span><span class="sxs-lookup"><span data-stu-id="a00e5-103">JET_OPENTEMPORARYTABLE.pidxunicode property</span></span>

<span data-ttu-id="a00e5-104">Возвращает или задает код локали и флаги нормализации, используемые для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="a00e5-104">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="a00e5-105">Если этот параметр имеет значение null, то для сравнения всех ключевых столбцов Юникода во временной таблице будет использоваться код по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a00e5-105">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="a00e5-106">По умолчанию используется языковой стандарт «Английский (США)».</span><span class="sxs-lookup"><span data-stu-id="a00e5-106">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="a00e5-107">Если этот параметр имеет значение null, то для сравнения данных любого ключевого столбца Юникода во временной таблице будут использоваться флаги нормализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a00e5-107">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="a00e5-108">Флаги нормализации по умолчанию: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="a00e5-108">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="a00e5-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a00e5-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="a00e5-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a00e5-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a00e5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a00e5-111">Syntax</span></span>

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="a00e5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a00e5-112">Property value</span></span>

<span data-ttu-id="a00e5-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="a00e5-113">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a00e5-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a00e5-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a00e5-115">Справочник</span><span class="sxs-lookup"><span data-stu-id="a00e5-115">Reference</span></span>

[<span data-ttu-id="a00e5-116">Класс JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="a00e5-116">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="a00e5-117">Элементы JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="a00e5-117">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="a00e5-118">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="a00e5-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
