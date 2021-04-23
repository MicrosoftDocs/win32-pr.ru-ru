---
description: Свойство Value объекта SWbemProperty определяет значение Variant свойства WMI. Это свойство автоматизации данного объекта по умолчанию.
ms.assetid: 547ec691-ff1c-4a6d-bee8-54e73d21cc93
ms.tgt_platform: multiple
title: Свойство SWbemProperty. Value (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Value
- ISWbemProperty.Value
- ISWbemProperty.get_Value
- ISWbemProperty.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e203929d0ce6ce98deff5ea89f9f226cd4cebfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998663"
---
# <a name="swbempropertyvalue-property"></a><span data-ttu-id="34cd0-104">SWbemProperty. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="34cd0-104">SWbemProperty.Value property</span></span>

<span data-ttu-id="34cd0-105">Свойство **value** объекта [**SWbemProperty**](swbemproperty.md) определяет значение Variant свойства WMI.</span><span class="sxs-lookup"><span data-stu-id="34cd0-105">The **Value** property of the [**SWbemProperty**](swbemproperty.md) object defines the variant value of the WMI property.</span></span> <span data-ttu-id="34cd0-106">Это свойство автоматизации данного объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34cd0-106">This is the default automation property of this object.</span></span>

<span data-ttu-id="34cd0-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="34cd0-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="34cd0-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="34cd0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="34cd0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34cd0-109">Syntax</span></span>


```VB
SWbemProperty.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="34cd0-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="34cd0-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="34cd0-111">Требования</span><span class="sxs-lookup"><span data-stu-id="34cd0-111">Requirements</span></span>



| <span data-ttu-id="34cd0-112">Требование</span><span class="sxs-lookup"><span data-stu-id="34cd0-112">Requirement</span></span> | <span data-ttu-id="34cd0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="34cd0-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34cd0-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34cd0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="34cd0-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34cd0-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34cd0-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34cd0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="34cd0-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34cd0-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34cd0-118">Header</span><span class="sxs-lookup"><span data-stu-id="34cd0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="34cd0-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34cd0-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="34cd0-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="34cd0-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="34cd0-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34cd0-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34cd0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="34cd0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34cd0-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34cd0-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="34cd0-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="34cd0-124">CLSID</span></span><br/>                    | <span data-ttu-id="34cd0-125">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="34cd0-125">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="34cd0-126">IID</span><span class="sxs-lookup"><span data-stu-id="34cd0-126">IID</span></span><br/>                      | <span data-ttu-id="34cd0-127">IID \_ исвбемпроперти</span><span class="sxs-lookup"><span data-stu-id="34cd0-127">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




