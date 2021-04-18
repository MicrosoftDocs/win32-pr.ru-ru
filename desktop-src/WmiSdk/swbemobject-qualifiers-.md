---
description: Свойство квалификаторов \_ объекта SWbemObject возвращает объект свбемкуалифиерсет, который является коллекцией квалификаторов для текущего класса или экземпляра. Это свойство доступно только для чтения.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Свойство SWbemObject.Qualifiers_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711642"
---
# <a name="swbemobjectqualifiers_-property"></a><span data-ttu-id="dfbc4-104">SWbemObject. квалификаторы, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="dfbc4-104">SWbemObject.Qualifiers\_ property</span></span>

<span data-ttu-id="dfbc4-105">Свойство **квалификаторов \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**свбемкуалифиерсет**](swbemqualifierset.md) , который является коллекцией квалификаторов для текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dfbc4-105">The **Qualifiers\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemQualifierSet**](swbemqualifierset.md) object that is a collection of the qualifiers for the current class or instance.</span></span> <span data-ttu-id="dfbc4-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dfbc4-106">This property is read-only.</span></span>

<span data-ttu-id="dfbc4-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dfbc4-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="dfbc4-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dfbc4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbc4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfbc4-109">Syntax</span></span>


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a><span data-ttu-id="dfbc4-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dfbc4-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="dfbc4-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="dfbc4-111">Examples</span></span>

<span data-ttu-id="dfbc4-112">[Список всех квалификаторов для](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) примера кода VBScript класса WMI в коллекции TechNet использует свойство квалификатора \_ для перечисления квалификаторов класса для указанного класса WMI.</span><span class="sxs-lookup"><span data-stu-id="dfbc4-112">The [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript code sample on TechNet Gallery uses the Qualifier\_ property to list the class qualifiers for a specified WMI class.</span></span>

<span data-ttu-id="dfbc4-113">В примере кода " [список всех абстрактных классов в инструментарии WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript" в галерее TechNet перечислены все абстрактные классы WMI, определенные в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="dfbc4-113">The [List All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript code sample on TechNet Gallery lists all WMI abstract classes defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="dfbc4-114">В примере кода для [всех динамических классов в инструментарии WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript используется свойство квалификатора \_ для перечисления всех динамических классов WMI (включая классы ассоциаций), определенных в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="dfbc4-114">The [List All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code sample uses the Qualifier\_ property to list all WMI Dynamic classes (including Association classes) defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="dfbc4-115">В примере кода PowerShell [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) в галерее TechNet перечислены все записываемые свойства в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="dfbc4-115">The [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell code sample on TechNet Gallery lists all writeable properties in the specified namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfbc4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dfbc4-116">Requirements</span></span>



| <span data-ttu-id="dfbc4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dfbc4-117">Requirement</span></span> | <span data-ttu-id="dfbc4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dfbc4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbc4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfbc4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dfbc4-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfbc4-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfbc4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfbc4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dfbc4-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfbc4-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfbc4-123">Header</span><span class="sxs-lookup"><span data-stu-id="dfbc4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfbc4-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbc4-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfbc4-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dfbc4-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="dfbc4-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dfbc4-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dfbc4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dfbc4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfbc4-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfbc4-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dfbc4-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="dfbc4-129">CLSID</span></span><br/>                    | <span data-ttu-id="dfbc4-130">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="dfbc4-130">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="dfbc4-131">IID</span><span class="sxs-lookup"><span data-stu-id="dfbc4-131">IID</span></span><br/>                      | <span data-ttu-id="dfbc4-132">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="dfbc4-132">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




