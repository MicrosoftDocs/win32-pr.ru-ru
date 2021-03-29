---
title: Обработка сфер и управление атрибутами
description: Обработка сфер, которая также называется манипуляцией с атрибутами, относится к преобразованию имени пользователя, запросившего доступ.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792576"
---
# <a name="realms-processing-and-attribute-manipulation"></a><span data-ttu-id="81373-103">Обработка сфер и управление атрибутами</span><span class="sxs-lookup"><span data-stu-id="81373-103">Realms Processing and Attribute Manipulation</span></span>

> [!Note]  
> <span data-ttu-id="81373-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="81373-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="81373-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="81373-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="81373-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="81373-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="81373-107">Обработка сфер, которая также называется манипуляцией с атрибутами, относится к преобразованию имени пользователя, запросившего доступ.</span><span class="sxs-lookup"><span data-stu-id="81373-107">Realms processing, which is also known as attribute manipulation, refers to transforming the name of the user requesting access.</span></span> <span data-ttu-id="81373-108">Также можно манипулировать ИДЕНТИФИКАТОРом вызывающей станции и ИДЕНТИФИКАТОРом вызываемой станции.</span><span class="sxs-lookup"><span data-stu-id="81373-108">The calling-station ID and called-station ID can also be manipulated.</span></span> <span data-ttu-id="81373-109">Правила обработки сфер являются частью коллекции атрибутов профиля прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="81373-109">The realms-processing rules are part of the Proxy profile attributes collection.</span></span>

<span data-ttu-id="81373-110">Для каждой манипуляции необходимо создать два атрибута для [правил манипуляции](/windows/desktop/Nps/sdo-manipulation-rule) .</span><span class="sxs-lookup"><span data-stu-id="81373-110">For each manipulation, you need to create two [Manipulation-Rule](/windows/desktop/Nps/sdo-manipulation-rule) attributes.</span></span> <span data-ttu-id="81373-111">Каждый из этих атрибутов является строковым значением.</span><span class="sxs-lookup"><span data-stu-id="81373-111">Each of these attributes is a string value.</span></span> <span data-ttu-id="81373-112">Первое правило содержит регулярное выражение, представляющее шаблон для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="81373-112">The first rule contains a regular expression representing the pattern to match.</span></span> <span data-ttu-id="81373-113">Второе правило содержит регулярное выражение, представляющее замещающий текст.</span><span class="sxs-lookup"><span data-stu-id="81373-113">The second rule contains a regular expression representing the replacement text.</span></span> <span data-ttu-id="81373-114">Необходимо также создать атрибут " [манипуляция-Target](/windows/desktop/Nps/sdo-manipulation-target) ".</span><span class="sxs-lookup"><span data-stu-id="81373-114">You must also create a [Manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) attribute.</span></span> <span data-ttu-id="81373-115">Этот атрибут является перечислением, которое указывает, какая часть данных пользователя будет управлять.</span><span class="sxs-lookup"><span data-stu-id="81373-115">This attribute is an enumeration that specifies which part of the user's information to manipulate.</span></span>

<span data-ttu-id="81373-116">Порядок, в котором создаются атрибуты, важен.</span><span class="sxs-lookup"><span data-stu-id="81373-116">The order in which the attributes are created is important.</span></span> <span data-ttu-id="81373-117">Сервер политики сети обрабатывает атрибуты в том порядке, в котором они были созданы.</span><span class="sxs-lookup"><span data-stu-id="81373-117">NPS processes the attributes in the order in which they were created.</span></span>

<span data-ttu-id="81373-118">В следующей таблице показан пример набора атрибутов манипуляции.</span><span class="sxs-lookup"><span data-stu-id="81373-118">The following table shows an example of a set of manipulation attributes.</span></span>



| <span data-ttu-id="81373-119">Имя</span><span class="sxs-lookup"><span data-stu-id="81373-119">Name</span></span>                 | <span data-ttu-id="81373-120">Тип</span><span class="sxs-lookup"><span data-stu-id="81373-120">Type</span></span>         | <span data-ttu-id="81373-121">Строковый параметр</span><span class="sxs-lookup"><span data-stu-id="81373-121">String Value</span></span>     |
|----------------------|--------------|------------------|
| <span data-ttu-id="81373-122">мсманипулатионруле</span><span class="sxs-lookup"><span data-stu-id="81373-122">msManipulationRule</span></span>   | <span data-ttu-id="81373-123">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="81373-123">**VT\_BSTR**</span></span> | <span data-ttu-id="81373-124">"@company.com"</span><span class="sxs-lookup"><span data-stu-id="81373-124">"@company.com"</span></span>   |
| <span data-ttu-id="81373-125">мсманипулатионруле</span><span class="sxs-lookup"><span data-stu-id="81373-125">msManipulationRule</span></span>   | <span data-ttu-id="81373-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="81373-126">**VT\_BSTR**</span></span> | <span data-ttu-id="81373-127">"@microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="81373-127">"@microsoft.com"</span></span> |
| <span data-ttu-id="81373-128">мсманипулатионруле</span><span class="sxs-lookup"><span data-stu-id="81373-128">msManipulationRule</span></span>   | <span data-ttu-id="81373-129">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="81373-129">**VT\_BSTR**</span></span> | <span data-ttu-id="81373-130">"^.+@"</span><span class="sxs-lookup"><span data-stu-id="81373-130">"^.+@"</span></span>           |
| <span data-ttu-id="81373-131">мсманипулатионруле</span><span class="sxs-lookup"><span data-stu-id="81373-131">msManipulationRule</span></span>   | <span data-ttu-id="81373-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="81373-132">**VT\_BSTR**</span></span> | <span data-ttu-id="81373-133">"guest@"</span><span class="sxs-lookup"><span data-stu-id="81373-133">"guest@"</span></span>         |
| <span data-ttu-id="81373-134">мсманипулатионтаржет</span><span class="sxs-lookup"><span data-stu-id="81373-134">msManipulationTarget</span></span> | <span data-ttu-id="81373-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="81373-135">**VT\_I4**</span></span>   | <span data-ttu-id="81373-136">"1"</span><span class="sxs-lookup"><span data-stu-id="81373-136">"1"</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="81373-137">См. также</span><span class="sxs-lookup"><span data-stu-id="81373-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81373-138">Иерархия объектной модели</span><span class="sxs-lookup"><span data-stu-id="81373-138">Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="81373-139">Поддерживаемые в SDO атрибуты</span><span class="sxs-lookup"><span data-stu-id="81373-139">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[<span data-ttu-id="81373-140">Создание политики запросов на подключение</span><span class="sxs-lookup"><span data-stu-id="81373-140">Creating a Connection Request Policy</span></span>](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[<span data-ttu-id="81373-141">**исдоколлектион**</span><span class="sxs-lookup"><span data-stu-id="81373-141">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="81373-142">**исдодиктионарйолд**</span><span class="sxs-lookup"><span data-stu-id="81373-142">**ISdoDictionaryOld**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[<span data-ttu-id="81373-143">**иаспропертиес**</span><span class="sxs-lookup"><span data-stu-id="81373-143">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 