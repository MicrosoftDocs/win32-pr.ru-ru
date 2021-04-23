---
description: Дополнительные сведения о методе API. JetInit2
title: API. JetInit2, метод
TOCTitle: 'JetInit2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit2(v=EXCHG.10)
ms:contentKeyID: 55100762
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 138a9830d5a74b887e7e68f3a3833f5f7e7fb8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712661"
---
# <a name="apijetinit2-method"></a><span data-ttu-id="7468e-103">API. JetInit2, метод</span><span class="sxs-lookup"><span data-stu-id="7468e-103">Api.JetInit2 method</span></span>

<span data-ttu-id="7468e-104">Инициализируйте ядро СУБД ESENT.</span><span class="sxs-lookup"><span data-stu-id="7468e-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="7468e-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7468e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7468e-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7468e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7468e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7468e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit2 ( _
    ByRef instance As JET_INSTANCE, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetInit2(instance, _
    grbit)
```

``` csharp
public static JET_wrn JetInit2(
    ref JET_INSTANCE instance,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7468e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7468e-108">Parameters</span></span>

  - <span data-ttu-id="7468e-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="7468e-109">instance</span></span>  
    <span data-ttu-id="7468e-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7468e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7468e-111">Экземпляр для инициализации.</span><span class="sxs-lookup"><span data-stu-id="7468e-111">The instance to initialize.</span></span> <span data-ttu-id="7468e-112">Если экземпляр не был выделен, создается новый, а ядро работает в режиме с одним экземпляром.</span><span class="sxs-lookup"><span data-stu-id="7468e-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="7468e-113">грбит</span><span class="sxs-lookup"><span data-stu-id="7468e-113">grbit</span></span>  
    <span data-ttu-id="7468e-114">Тип: [Microsoft.Isam.Esent.Interop.Iniтгрбит](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7468e-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7468e-115">Параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="7468e-115">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7468e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7468e-116">Return value</span></span>

<span data-ttu-id="7468e-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7468e-117">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="7468e-118">Код предупреждения.</span><span class="sxs-lookup"><span data-stu-id="7468e-118">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7468e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7468e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7468e-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="7468e-120">Reference</span></span>

[<span data-ttu-id="7468e-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="7468e-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7468e-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="7468e-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7468e-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7468e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
