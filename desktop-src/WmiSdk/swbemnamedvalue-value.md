---
description: Свойство Value объекта Свбемнамедвалуе возвращает значение типа Variant элемента Свбемнамедвалуе.
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.tgt_platform: multiple
title: Свойство Свбемнамедвалуе. Value (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue.Value
- ISWbemNamedValue.Value
- ISWbemNamedValue.get_Value
- ISWbemNamedValue.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bf63b15a27c1149341200f29e938bdba6cd7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155834"
---
# <a name="swbemnamedvaluevalue-property"></a><span data-ttu-id="a2497-103">Свбемнамедвалуе. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="a2497-103">SWbemNamedValue.Value property</span></span>

<span data-ttu-id="a2497-104">Свойство **value** объекта [**свбемнамедвалуе**](swbemnamedvalue.md) возвращает значение типа Variant элемента **свбемнамедвалуе** .</span><span class="sxs-lookup"><span data-stu-id="a2497-104">The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item.</span></span> <span data-ttu-id="a2497-105">Это свойство по умолчанию для объектов **свбемнамедвалуе** .</span><span class="sxs-lookup"><span data-stu-id="a2497-105">This is the default property for **SWbemNamedValue** objects.</span></span> <span data-ttu-id="a2497-106">Изменения, вносимые в свойство Value, автоматически отражаются в коллекции [**свбемнамедвалуесет**](swbemnamedvalueset.md) , к которой принадлежит объект **свбемнамедвалуе** .</span><span class="sxs-lookup"><span data-stu-id="a2497-106">Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.</span></span>

<span data-ttu-id="a2497-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a2497-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a2497-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a2497-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2497-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2497-109">Syntax</span></span>


```VB
SWbemNamedValue.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="a2497-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a2497-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a2497-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a2497-111">Requirements</span></span>



| <span data-ttu-id="a2497-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a2497-112">Requirement</span></span> | <span data-ttu-id="a2497-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a2497-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2497-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2497-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a2497-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2497-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2497-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2497-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a2497-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2497-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2497-118">Header</span><span class="sxs-lookup"><span data-stu-id="a2497-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2497-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2497-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2497-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a2497-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2497-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a2497-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a2497-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a2497-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2497-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2497-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a2497-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="a2497-124">CLSID</span></span><br/>                    | <span data-ttu-id="a2497-125">\_СВБЕМНАМЕДВАЛУЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="a2497-125">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="a2497-126">IID</span><span class="sxs-lookup"><span data-stu-id="a2497-126">IID</span></span><br/>                      | <span data-ttu-id="a2497-127">IID \_ исвбемнамедвалуе</span><span class="sxs-lookup"><span data-stu-id="a2497-127">IID\_ISWbemNamedValue</span></span><br/>                                                        |



 

 




