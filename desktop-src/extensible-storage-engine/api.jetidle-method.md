---
description: Дополнительные сведения о методе API. Жетидле
title: API. Жетидле, метод
TOCTitle: 'JetIdle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIdle(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.IdleGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetidle(v=EXCHG.10)
ms:contentKeyID: 55100757
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e524a23d5e8fb20b1b6db1fb7e82fbb07bf3df0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999552"
---
# <a name="apijetidle-method"></a><span data-ttu-id="9068e-103">API. Жетидле, метод</span><span class="sxs-lookup"><span data-stu-id="9068e-103">Api.JetIdle method</span></span>

<span data-ttu-id="9068e-104">Выполняет задачи очистки при простое или проверяет состояние хранилища версий в ESE.</span><span class="sxs-lookup"><span data-stu-id="9068e-104">Performs idle cleanup tasks or checks the version store status in ESE.</span></span>

<span data-ttu-id="9068e-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9068e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9068e-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9068e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9068e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9068e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetIdle ( _
    sesid As JET_SESID, _
    grbit As IdleGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim grbit As IdleGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetIdle(sesid, _
    grbit)
```

``` csharp
public static JET_wrn JetIdle(
    JET_SESID sesid,
    IdleGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9068e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9068e-108">Parameters</span></span>

  - <span data-ttu-id="9068e-109">сесид</span><span class="sxs-lookup"><span data-stu-id="9068e-109">sesid</span></span>  
    <span data-ttu-id="9068e-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9068e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9068e-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="9068e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9068e-112">грбит</span><span class="sxs-lookup"><span data-stu-id="9068e-112">grbit</span></span>  
    <span data-ttu-id="9068e-113">Тип: [Microsoft. ISAM. ESENT. Interop. идлегрбит](./idlegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9068e-113">Type: [Microsoft.Isam.Esent.Interop.IdleGrbit](./idlegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9068e-114">Сочетание флагов Жетидлегрбит.</span><span class="sxs-lookup"><span data-stu-id="9068e-114">A combination of JetIdleGrbit flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9068e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9068e-115">Return value</span></span>

<span data-ttu-id="9068e-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9068e-116">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="9068e-117">Код ошибки, если операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9068e-117">An error code if the operation fails.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9068e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9068e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9068e-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="9068e-119">Reference</span></span>

[<span data-ttu-id="9068e-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="9068e-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9068e-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="9068e-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9068e-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9068e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
