---
description: Свойство Name объекта Свбемпривилеже — это строка, которая уникально описывает привилегии.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Свойство SWbemPrivilege.Name (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272557"
---
# <a name="swbemprivilegename-property"></a><span data-ttu-id="48826-103">SWbemPrivilege.Name, свойство</span><span class="sxs-lookup"><span data-stu-id="48826-103">SWbemPrivilege.Name property</span></span>

<span data-ttu-id="48826-104">Свойство **Name** объекта [**свбемпривилеже**](swbemprivilege.md) — это строка, которая уникально описывает привилегии.</span><span class="sxs-lookup"><span data-stu-id="48826-104">The **Name** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that uniquely describes a privilege.</span></span> <span data-ttu-id="48826-105">Например, привилегия, определяющая, может ли пользователь выполнить метод завершения работы объекта, имеет строку "Сешутдовнпривилеже" в свойстве **SWbemPrivilege.Name** .</span><span class="sxs-lookup"><span data-stu-id="48826-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the **SWbemPrivilege.Name** property.</span></span> <span data-ttu-id="48826-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="48826-106">This property is read-only.</span></span>

<span data-ttu-id="48826-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="48826-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="48826-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="48826-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="48826-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48826-109">Syntax</span></span>


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a><span data-ttu-id="48826-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="48826-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="48826-111">Требования</span><span class="sxs-lookup"><span data-stu-id="48826-111">Requirements</span></span>



| <span data-ttu-id="48826-112">Требование</span><span class="sxs-lookup"><span data-stu-id="48826-112">Requirement</span></span> | <span data-ttu-id="48826-113">Значение</span><span class="sxs-lookup"><span data-stu-id="48826-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48826-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48826-114">Minimum supported client</span></span><br/> | <span data-ttu-id="48826-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48826-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48826-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48826-116">Minimum supported server</span></span><br/> | <span data-ttu-id="48826-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48826-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48826-118">Header</span><span class="sxs-lookup"><span data-stu-id="48826-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="48826-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48826-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48826-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="48826-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="48826-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48826-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="48826-122">DLL</span><span class="sxs-lookup"><span data-stu-id="48826-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48826-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48826-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="48826-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="48826-124">CLSID</span></span><br/>                    | <span data-ttu-id="48826-125">\_СВБЕМПРИВИЛЕЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="48826-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="48826-126">IID</span><span class="sxs-lookup"><span data-stu-id="48826-126">IID</span></span><br/>                      | <span data-ttu-id="48826-127">IID \_ исвбемпривилеже</span><span class="sxs-lookup"><span data-stu-id="48826-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




