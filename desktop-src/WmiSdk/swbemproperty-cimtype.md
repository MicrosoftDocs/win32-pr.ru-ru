---
description: Свойство Цимтипе объекта SWbemProperty — это целое число, которое можно использовать для определения типа CIM этого свойства. Это свойство доступно только для чтения.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Свойство SWbemProperty. Цимтипе (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998664"
---
# <a name="swbempropertycimtype-property"></a><span data-ttu-id="15e29-104">SWbemProperty. Цимтипе, свойство</span><span class="sxs-lookup"><span data-stu-id="15e29-104">SWbemProperty.CIMType property</span></span>

<span data-ttu-id="15e29-105">Свойство **Цимтипе** объекта [**SWbemProperty**](swbemproperty.md) — это целое число, которое можно использовать для определения типа CIM этого свойства.</span><span class="sxs-lookup"><span data-stu-id="15e29-105">The **CIMType** property of the [**SWbemProperty**](swbemproperty.md) object is an integer that can be used to determine the CIM type of this property.</span></span> <span data-ttu-id="15e29-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="15e29-106">This property is read-only.</span></span>

<span data-ttu-id="15e29-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="15e29-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="15e29-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="15e29-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e29-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15e29-109">Syntax</span></span>


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a><span data-ttu-id="15e29-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="15e29-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="15e29-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15e29-111">Remarks</span></span>

<span data-ttu-id="15e29-112">Дополнительные сведения о допустимых типах для этого свойства см. в разделе [**вбемЦимтипинум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="15e29-112">For more information about valid types for this property, see [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>

<span data-ttu-id="15e29-113">Экземпляры внедренных объектов хранятся в составных объектах в виде свойств типа **\_ объекта CIM**.</span><span class="sxs-lookup"><span data-stu-id="15e29-113">Instances of embedded objects are stored in composite objects as properties of type **CIM\_OBJECT**.</span></span> <span data-ttu-id="15e29-114">Чтобы определить класс внедренного объекта в экземпляре составного класса, необходимо изучить квалификатор **Цимтипе** свойства типа **\_ объекта CIM** .</span><span class="sxs-lookup"><span data-stu-id="15e29-114">To determine the class of an embedded object in an instance of a composite class, you must examine the **CIMType** qualifier of the **CIM\_OBJECT** type property.</span></span>

<span data-ttu-id="15e29-115">Ссылки на объекты в классе ассоциации хранятся в свойствах типа " **\_ ссылка на CIM**".</span><span class="sxs-lookup"><span data-stu-id="15e29-115">The object references in an association class are stored in properties of type **CIM\_REFERENCE**.</span></span> <span data-ttu-id="15e29-116">Чтобы определить фактические пути к объекту, необходимо проверить квалификатор **Цимтипе** свойства **\_ ссылочного типа CIM** .</span><span class="sxs-lookup"><span data-stu-id="15e29-116">To determine the actual object paths you must examine the **CIMType** qualifier of the **CIM\_REFERENCE** type property.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e29-117">Требования</span><span class="sxs-lookup"><span data-stu-id="15e29-117">Requirements</span></span>



| <span data-ttu-id="15e29-118">Требование</span><span class="sxs-lookup"><span data-stu-id="15e29-118">Requirement</span></span> | <span data-ttu-id="15e29-119">Значение</span><span class="sxs-lookup"><span data-stu-id="15e29-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15e29-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15e29-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15e29-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15e29-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15e29-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15e29-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15e29-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15e29-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15e29-124">Header</span><span class="sxs-lookup"><span data-stu-id="15e29-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e29-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="15e29-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15e29-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="15e29-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="15e29-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15e29-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15e29-128">DLL</span><span class="sxs-lookup"><span data-stu-id="15e29-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15e29-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e29-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15e29-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="15e29-130">CLSID</span></span><br/>                    | <span data-ttu-id="15e29-131">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="15e29-131">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="15e29-132">IID</span><span class="sxs-lookup"><span data-stu-id="15e29-132">IID</span></span><br/>                      | <span data-ttu-id="15e29-133">IID \_ исвбемпроперти</span><span class="sxs-lookup"><span data-stu-id="15e29-133">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




