---
description: Динамический квалификатор указывает класс, экземпляры которого создаются динамически. Значение этого квалификатора должно быть равно TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Динамический квалификатор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898790"
---
# <a name="dynamic-qualifier"></a><span data-ttu-id="54126-104">Динамический квалификатор</span><span class="sxs-lookup"><span data-stu-id="54126-104">Dynamic Qualifier</span></span>

<span data-ttu-id="54126-105">**Динамический** квалификатор указывает класс, экземпляры которого создаются динамически.</span><span class="sxs-lookup"><span data-stu-id="54126-105">The **Dynamic** qualifier indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="54126-106">Значение этого квалификатора должно быть равно **true**.</span><span class="sxs-lookup"><span data-stu-id="54126-106">The value of this qualifier must be set to **TRUE**.</span></span>

<span data-ttu-id="54126-107">**Динамический** квалификатор должен быть указан во всех классах, содержащих данные, и для которых экземпляры создаются динамически.</span><span class="sxs-lookup"><span data-stu-id="54126-107">The **Dynamic** qualifier must be specified on all classes that contain data and for which instances are created dynamically.</span></span> <span data-ttu-id="54126-108">Квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) , как правило, также указывается для указания поставщика, ответственного за предоставление данных.</span><span class="sxs-lookup"><span data-stu-id="54126-108">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is typically also specified to identify the provider responsible for supplying the data.</span></span>

<span data-ttu-id="54126-109">Классы, содержащие только те методы, которые нуждаются в реализации, не требуют **динамического** квалификатора.</span><span class="sxs-lookup"><span data-stu-id="54126-109">Classes that contain only methods that need implementation do not require the **Dynamic** qualifier.</span></span> <span data-ttu-id="54126-110">Для указания имени поставщика, предоставляющего реализацию, требуется только квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="54126-110">Only the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is required to specify the name of the provider to supply the implementation.</span></span>

<span data-ttu-id="54126-111">Все классы, производные от динамического класса, должны быть динамическими.</span><span class="sxs-lookup"><span data-stu-id="54126-111">All classes derived from a dynamic class must be dynamic.</span></span> <span data-ttu-id="54126-112">Нельзя наследовать статический класс от динамического класса.</span><span class="sxs-lookup"><span data-stu-id="54126-112">You cannot derive a static class from a dynamic class.</span></span>

<span data-ttu-id="54126-113">Если для свойства экземпляра задано значение **dynamic** , также должен быть указан квалификатор **пропертиконтекст** .</span><span class="sxs-lookup"><span data-stu-id="54126-113">When **Dynamic** is specified on a property of an instance, the **PropertyContext** qualifier must also be specified.</span></span>

## <a name="requirements"></a><span data-ttu-id="54126-114">Требования</span><span class="sxs-lookup"><span data-stu-id="54126-114">Requirements</span></span>



| <span data-ttu-id="54126-115">Требование</span><span class="sxs-lookup"><span data-stu-id="54126-115">Requirement</span></span> | <span data-ttu-id="54126-116">Значение</span><span class="sxs-lookup"><span data-stu-id="54126-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="54126-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54126-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54126-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54126-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="54126-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54126-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54126-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54126-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54126-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54126-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54126-122">**Стандартные квалификаторы WMI**</span><span class="sxs-lookup"><span data-stu-id="54126-122">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="54126-123">Квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="54126-123">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="54126-124">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="54126-124">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




