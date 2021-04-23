---
description: Этот раздел относится к пакету обновления 2 (SP2) для Windows XP или более поздней версии. \_Структура подключения кстопологи описывает соединение узла в фильтре потоковой передачи (KS). Узел можно подключить к другому узлу в фильтре или к закрепления фильтра.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: Структура KSTOPOLOGY_CONNECTION (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689078"
---
# <a name="kstopology_connection-structure"></a><span data-ttu-id="bf2ba-105">\_Структура подключения кстопологи</span><span class="sxs-lookup"><span data-stu-id="bf2ba-105">KSTOPOLOGY\_CONNECTION structure</span></span>

<span data-ttu-id="bf2ba-106">Этот раздел относится к пакету обновления 2 (SP2) для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-106">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="bf2ba-107">Структура **\_ подключения кстопологи** описывает соединение узла в фильтре потоковой передачи (KS).</span><span class="sxs-lookup"><span data-stu-id="bf2ba-107">The **KSTOPOLOGY\_CONNECTION** structure describes a node connection within a kernel-streaming (KS) filter.</span></span> <span data-ttu-id="bf2ba-108">Узел можно подключить к другому узлу в фильтре или к закрепления фильтра.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-108">A node can be connected to another node within the filter, or to a pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2ba-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf2ba-109">Syntax</span></span>


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a><span data-ttu-id="bf2ba-110">Члены</span><span class="sxs-lookup"><span data-stu-id="bf2ba-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf2ba-111">**фромноде**</span><span class="sxs-lookup"><span data-stu-id="bf2ba-111">**FromNode**</span></span>
</dt> <dd>

<span data-ttu-id="bf2ba-112">Индекс вышестоящего узла в соединении.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-112">Index of the upstream node in the connection.</span></span> <span data-ttu-id="bf2ba-113">Если вышестоящее соединение является ПИН-кодом, а не узлом, значением является КСФИЛТЕР \_ node.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-113">If the upstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ba-114">**фромнодепин**</span><span class="sxs-lookup"><span data-stu-id="bf2ba-114">**FromNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="bf2ba-115">Если значение поля **фромноде** равно ксфилтер \_ Node, то в этом поле указывается индекс вышестоящего ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-115">If the value of the **FromNode** field is KSFILTER\_NODE, this field specifies the index of the upstream pin.</span></span> <span data-ttu-id="bf2ba-116">В противном случае это поле игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-116">Otherwise, this field is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ba-117">**тоноде**</span><span class="sxs-lookup"><span data-stu-id="bf2ba-117">**ToNode**</span></span>
</dt> <dd>

<span data-ttu-id="bf2ba-118">Индекс подчиненного узла в соединении.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-118">Index of the downstream node in the connection.</span></span> <span data-ttu-id="bf2ba-119">Если подчиненное соединение является ПИН-кодом, а не узлом, то значением является КСФИЛТЕР \_ node.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-119">If the downstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ba-120">**тонодепин**</span><span class="sxs-lookup"><span data-stu-id="bf2ba-120">**ToNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="bf2ba-121">Если значение поля **тоноде** равно ксфилтер \_ Node, то в этом поле указывается индекс подчиненного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-121">If the value of the **ToNode** field is KSFILTER\_NODE, this field specifies the index of the downstream pin.</span></span> <span data-ttu-id="bf2ba-122">В противном случае это поле игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bf2ba-122">Otherwise, this field is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf2ba-123">Требования</span><span class="sxs-lookup"><span data-stu-id="bf2ba-123">Requirements</span></span>



| <span data-ttu-id="bf2ba-124">Требование</span><span class="sxs-lookup"><span data-stu-id="bf2ba-124">Requirement</span></span> | <span data-ttu-id="bf2ba-125">Значение</span><span class="sxs-lookup"><span data-stu-id="bf2ba-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="bf2ba-126">Header</span><span class="sxs-lookup"><span data-stu-id="bf2ba-126">Header</span></span><br/> | <dl> <span data-ttu-id="bf2ba-127"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ba-127"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2ba-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf2ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2ba-129">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf2ba-129">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="bf2ba-130">**Икстопологинфо:: Get \_ ConnectionInfo**</span><span class="sxs-lookup"><span data-stu-id="bf2ba-130">**IKsTopologyInfo::get\_ConnectionInfo**</span></span>](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




