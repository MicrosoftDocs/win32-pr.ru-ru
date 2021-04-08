---
description: 'Дополнительные сведения о методе: Вистаапи. ЖетжетинстанцемисЦинфо'
title: Вистаапи. ЖетжетинстанцемисЦинфо, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898461"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a><span data-ttu-id="660ae-103">Вистаапи. ЖетжетинстанцемисЦинфо, метод</span><span class="sxs-lookup"><span data-stu-id="660ae-103">VistaApi.JetGetInstanceMiscInfo method</span></span>

<span data-ttu-id="660ae-104">Извлекает сведения об экземпляре.</span><span class="sxs-lookup"><span data-stu-id="660ae-104">Retrieves information about an instance.</span></span>

<span data-ttu-id="660ae-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="660ae-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="660ae-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="660ae-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="660ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="660ae-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="660ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="660ae-108">Parameters</span></span>

  - <span data-ttu-id="660ae-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="660ae-109">instance</span></span>  
    <span data-ttu-id="660ae-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="660ae-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="660ae-111">Экземпляр, сведения о котором необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="660ae-111">The instance to get information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="660ae-112">подпись</span><span class="sxs-lookup"><span data-stu-id="660ae-112">signature</span></span>  
    <span data-ttu-id="660ae-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="660ae-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="660ae-114">Извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="660ae-114">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="660ae-115">инфолевел</span><span class="sxs-lookup"><span data-stu-id="660ae-115">infoLevel</span></span>  
    <span data-ttu-id="660ae-116">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="660ae-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="660ae-117">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="660ae-117">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="660ae-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="660ae-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="660ae-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="660ae-119">Reference</span></span>

[<span data-ttu-id="660ae-120">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="660ae-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="660ae-121">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="660ae-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="660ae-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="660ae-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
