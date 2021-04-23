---
description: 'Дополнительные сведения о методе: Вистаапи. JetInit3'
title: Вистаапи. JetInit3, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c5fa7d1450240a8250e66e2bbe6d8ef0b97c136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701649"
---
# <a name="vistaapijetinit3-method"></a><span data-ttu-id="bc7e6-103">Вистаапи. JetInit3, метод</span><span class="sxs-lookup"><span data-stu-id="bc7e6-103">VistaApi.JetInit3 method</span></span>

<span data-ttu-id="bc7e6-104">Инициализируйте ядро СУБД ESENT.</span><span class="sxs-lookup"><span data-stu-id="bc7e6-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="bc7e6-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc7e6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="bc7e6-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc7e6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7e6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc7e6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bc7e6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc7e6-108">Parameters</span></span>

  - <span data-ttu-id="bc7e6-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="bc7e6-109">instance</span></span>  
    <span data-ttu-id="bc7e6-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc7e6-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="bc7e6-111">Экземпляр для инициализации.</span><span class="sxs-lookup"><span data-stu-id="bc7e6-111">The instance to initialize.</span></span> <span data-ttu-id="bc7e6-112">Если экземпляр не был выделен, создается новый, а ядро работает в режиме с одним экземпляром.</span><span class="sxs-lookup"><span data-stu-id="bc7e6-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc7e6-113">рековерйоптионс</span><span class="sxs-lookup"><span data-stu-id="bc7e6-113">recoveryOptions</span></span>  
    <span data-ttu-id="bc7e6-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="bc7e6-114">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="bc7e6-115">Дополнительные параметры восстановления для повторного сопоставления баз данных во время восстановления, расположение для отмены восстановления или состояние восстановления.</span><span class="sxs-lookup"><span data-stu-id="bc7e6-115">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc7e6-116">грбит</span><span class="sxs-lookup"><span data-stu-id="bc7e6-116">grbit</span></span>  
    <span data-ttu-id="bc7e6-117">Тип: [Microsoft.Isam.Esent.Interop.Iniтгрбит](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bc7e6-117">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bc7e6-118">Параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="bc7e6-118">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="bc7e6-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc7e6-119">Return value</span></span>

<span data-ttu-id="bc7e6-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bc7e6-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="bc7e6-121">Код предупреждения.</span><span class="sxs-lookup"><span data-stu-id="bc7e6-121">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bc7e6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc7e6-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc7e6-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="bc7e6-123">Reference</span></span>

[<span data-ttu-id="bc7e6-124">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="bc7e6-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="bc7e6-125">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="bc7e6-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="bc7e6-126">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="bc7e6-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
