---
description: Свойство Origin объекта SWbemProperty извлекает имя класса WMI, в котором было введено это свойство. Для классов с иерархиями с глубоким наследованием часто желательно выяснить, какие свойства были объявлены в каких классах.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Свойство SWbemProperty. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264796"
---
# <a name="swbempropertyorigin-property"></a><span data-ttu-id="96222-104">SWbemProperty. Origin, свойство</span><span class="sxs-lookup"><span data-stu-id="96222-104">SWbemProperty.Origin property</span></span>

<span data-ttu-id="96222-105">Свойство **Origin** объекта [**SWbemProperty**](swbemproperty.md) извлекает имя класса WMI, в котором было введено это свойство.</span><span class="sxs-lookup"><span data-stu-id="96222-105">The **Origin** property of the [**SWbemProperty**](swbemproperty.md) object retrieves the name of the WMI class in which this property was introduced.</span></span> <span data-ttu-id="96222-106">Для классов с иерархиями с глубоким наследованием часто желательно выяснить, какие свойства были объявлены в каких классах.</span><span class="sxs-lookup"><span data-stu-id="96222-106">For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.</span></span>

<span data-ttu-id="96222-107">Если свойство является локальным (см [**. свбемкуалифиер. local**](swbemqualifier-islocal.md)), это значение совпадает с классом-владельцем.</span><span class="sxs-lookup"><span data-stu-id="96222-107">If the property is local (see [**SWbemQualifier.IsLocal**](swbemqualifier-islocal.md)), this value is the same as the owning class.</span></span> <span data-ttu-id="96222-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="96222-108">This property is read-only.</span></span>

<span data-ttu-id="96222-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="96222-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="96222-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="96222-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="96222-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96222-111">Syntax</span></span>


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="96222-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="96222-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="96222-113">Требования</span><span class="sxs-lookup"><span data-stu-id="96222-113">Requirements</span></span>



| <span data-ttu-id="96222-114">Требование</span><span class="sxs-lookup"><span data-stu-id="96222-114">Requirement</span></span> | <span data-ttu-id="96222-115">Значение</span><span class="sxs-lookup"><span data-stu-id="96222-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96222-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96222-116">Minimum supported client</span></span><br/> | <span data-ttu-id="96222-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96222-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96222-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96222-118">Minimum supported server</span></span><br/> | <span data-ttu-id="96222-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96222-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96222-120">Header</span><span class="sxs-lookup"><span data-stu-id="96222-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="96222-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="96222-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="96222-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="96222-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="96222-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="96222-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="96222-124">DLL</span><span class="sxs-lookup"><span data-stu-id="96222-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96222-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96222-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="96222-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="96222-126">CLSID</span></span><br/>                    | <span data-ttu-id="96222-127">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="96222-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="96222-128">IID</span><span class="sxs-lookup"><span data-stu-id="96222-128">IID</span></span><br/>                      | <span data-ttu-id="96222-129">IID \_ исвбемпроперти</span><span class="sxs-lookup"><span data-stu-id="96222-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




