---
description: 'Дополнительные сведения о методе: Windows8Api. Жетсетсессионпараметер'
title: Windows8Api. Жетсетсессионпараметер, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetSetSessionParameter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetsessionparameter(v=EXCHG.10)
ms:contentKeyID: 55104461
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b73331c765e1f8026b39c28dde5268417601663c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898066"
---
# <a name="windows8apijetsetsessionparameter-method"></a><span data-ttu-id="1d502-103">Windows8Api. Жетсетсессионпараметер, метод</span><span class="sxs-lookup"><span data-stu-id="1d502-103">Windows8Api.JetSetSessionParameter method</span></span>

<span data-ttu-id="1d502-104">Задает параметр для указанного состояния сеанса, используемый в течение времени существования этого сеанса или до сброса.</span><span class="sxs-lookup"><span data-stu-id="1d502-104">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span>

<span data-ttu-id="1d502-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1d502-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="1d502-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1d502-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1d502-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d502-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionParameter ( _
    sesid As JET_SESID, _
    sesparamid As JET_sesparam, _
    data As Byte(), _
    dataSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim sesparamid As JET_sesparam
Dim data As Byte()
Dim dataSize As IntegerWindows8Api.JetSetSessionParameter(sesid, _
    sesparamid, data, dataSize)
```

``` csharp
public static void JetSetSessionParameter(
    JET_SESID sesid,
    JET_sesparam sesparamid,
    byte[] data,
    int dataSize
)
```

#### <a name="parameters"></a><span data-ttu-id="1d502-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d502-108">Parameters</span></span>

  - <span data-ttu-id="1d502-109">сесид</span><span class="sxs-lookup"><span data-stu-id="1d502-109">sesid</span></span>  
    <span data-ttu-id="1d502-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d502-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1d502-111">Сеанс, для которого задается параметр.</span><span class="sxs-lookup"><span data-stu-id="1d502-111">The session to set the parameter on.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d502-112">сеспарамид</span><span class="sxs-lookup"><span data-stu-id="1d502-112">sesparamid</span></span>  
    <span data-ttu-id="1d502-113">Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1d502-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span></span>  
    
    <span data-ttu-id="1d502-114">ИДЕНТИФИКАТОР устанавливаемого параметра сеанса.</span><span class="sxs-lookup"><span data-stu-id="1d502-114">The ID of the session parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d502-115">.</span><span class="sxs-lookup"><span data-stu-id="1d502-115">data</span></span>  
    <span data-ttu-id="1d502-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="1d502-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="1d502-117">Данные, которые необходимо задать в этом параметре сеанса.</span><span class="sxs-lookup"><span data-stu-id="1d502-117">Data to set in this session parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d502-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="1d502-118">dataSize</span></span>  
    <span data-ttu-id="1d502-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1d502-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1d502-120">Размер предоставленных данных.</span><span class="sxs-lookup"><span data-stu-id="1d502-120">Size of the data provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d502-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d502-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1d502-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="1d502-122">Reference</span></span>

[<span data-ttu-id="1d502-123">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="1d502-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="1d502-124">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="1d502-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="1d502-125">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="1d502-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
