---
description: Свойство Origin объекта Свбеммесод возвращает имя класса, в котором был представлен этот метод.
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: Свойство Свбеммесод. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263802"
---
# <a name="swbemmethodorigin-property"></a><span data-ttu-id="bdd45-103">Свбеммесод. Origin, свойство</span><span class="sxs-lookup"><span data-stu-id="bdd45-103">SWbemMethod.Origin property</span></span>

<span data-ttu-id="bdd45-104">Свойство **Origin** объекта [**свбеммесод**](swbemmethod.md) возвращает имя класса, в котором был представлен этот метод.</span><span class="sxs-lookup"><span data-stu-id="bdd45-104">The **Origin** property of the [**SWbemMethod**](swbemmethod.md) object returns the name of the class in which this method was introduced.</span></span> <span data-ttu-id="bdd45-105">Для классов с иерархиями с глубоким наследованием часто желательно понять, какие методы были объявлены в каких классах.</span><span class="sxs-lookup"><span data-stu-id="bdd45-105">For classes with deep inheritance hierarchies, it is often desirable to know which methods were declared in which classes.</span></span> <span data-ttu-id="bdd45-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bdd45-106">This property is read-only.</span></span>

<span data-ttu-id="bdd45-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bdd45-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bdd45-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bdd45-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd45-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdd45-109">Syntax</span></span>


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="bdd45-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bdd45-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd45-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bdd45-111">Requirements</span></span>



| <span data-ttu-id="bdd45-112">Требование</span><span class="sxs-lookup"><span data-stu-id="bdd45-112">Requirement</span></span> | <span data-ttu-id="bdd45-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bdd45-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd45-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdd45-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd45-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bdd45-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bdd45-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdd45-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd45-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdd45-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bdd45-118">Header</span><span class="sxs-lookup"><span data-stu-id="bdd45-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdd45-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdd45-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdd45-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bdd45-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="bdd45-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bdd45-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bdd45-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bdd45-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdd45-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdd45-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bdd45-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="bdd45-124">CLSID</span></span><br/>                    | <span data-ttu-id="bdd45-125">\_СВБЕММЕСОД CLSID</span><span class="sxs-lookup"><span data-stu-id="bdd45-125">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="bdd45-126">IID</span><span class="sxs-lookup"><span data-stu-id="bdd45-126">IID</span></span><br/>                      | <span data-ttu-id="bdd45-127">IID \_ исвбеммесод</span><span class="sxs-lookup"><span data-stu-id="bdd45-127">IID\_ISWbemMethod</span></span><br/>                                                            |



 

 




