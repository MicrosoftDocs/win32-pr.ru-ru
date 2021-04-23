---
description: Сетевой монитор предоставляет структуру PROPERTYINFO для определения свойств протокола, а также структуры ПРОПЕРТИНСТ и ПРОПЕРТИНСТЕКС для определения экземпляра свойства.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Структуры свойств и экземпляров свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813307"
---
# <a name="property-definition-and-property-instance-structures"></a><span data-ttu-id="93166-103">Структуры свойств и экземпляров свойств</span><span class="sxs-lookup"><span data-stu-id="93166-103">Property Definition and Property Instance Structures</span></span>

<span data-ttu-id="93166-104">Сетевой монитор предоставляет структуру [**PROPERTYINFO**](propertyinfo.md) для определения свойств протокола, а также структуры [**пропертинст**](propertyinst.md)и [**пропертинстекс**](propertyinstex.md) для определения экземпляра свойства.</span><span class="sxs-lookup"><span data-stu-id="93166-104">Network Monitor provides a [**PROPERTYINFO**](propertyinfo.md) structure to define the properties of a protocol, and a [**PROPERTYINST**](propertyinst.md), and [**PROPERTYINSTEX**](propertyinstex.md) structure to define an instance of a property.</span></span>

![структуры сетевого монитора](images/property1.png)

<span data-ttu-id="93166-106">Средство синтаксического анализа выделяет и заполняет структуру [**PROPERTYINFO**](propertyinfo.md) для всех свойств, поддерживаемых протоколом.</span><span class="sxs-lookup"><span data-stu-id="93166-106">The parser allocates and fills-in the [**PROPERTYINFO**](propertyinfo.md) structure for all the properties that a protocol supports.</span></span> <span data-ttu-id="93166-107">Средство синтаксического анализа передает структуру в сетевой монитор, где структура добавляется в [*базу данных свойств*](p.md)протокола.</span><span class="sxs-lookup"><span data-stu-id="93166-107">The parser passes the structure to Network Monitor where the structure is added to the protocol [*property database*](p.md).</span></span> <span data-ttu-id="93166-108">Сведения в структуре **PROPERTYINFO** используются при анализе экземпляра свойства, а также при форматировании данных, отображаемых в сетевой монитор пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="93166-108">The information in the **PROPERTYINFO** structure is used when parsing an instance of a property, and when formatting the data that is displayed in the Network Monitor UI.</span></span>

<span data-ttu-id="93166-109">Сетевой монитор выделяет структуры [**пропертинст**](propertyinst.md) и [**пропертинстекс**](propertyinstex.md) , когда средство синтаксического анализа прикрепляет определение свойства к экземпляру свойства.</span><span class="sxs-lookup"><span data-stu-id="93166-109">Network Monitor allocates the [**PROPERTYINST**](propertyinst.md) and [**PROPERTYINSTEX**](propertyinstex.md) structures when the parser attaches a property definition to an instance of a property.</span></span>

<span data-ttu-id="93166-110">Следующая процедура определяет шаги, необходимые для присоединения определения свойства.</span><span class="sxs-lookup"><span data-stu-id="93166-110">The following procedure identifies the steps necessary to attach a property definition.</span></span>

<span data-ttu-id="93166-111">**Присоединение определения свойства**</span><span class="sxs-lookup"><span data-stu-id="93166-111">**To attach a property definition**</span></span>

1.  <span data-ttu-id="93166-112">Определяет каждое свойство, существующее в экземпляре протокола.</span><span class="sxs-lookup"><span data-stu-id="93166-112">Identify each property that exists in an instance of the protocol.</span></span> <span data-ttu-id="93166-113">При присоединении определения сетевой монитор передает захваченные данные в средство синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="93166-113">When attaching a definition, Network Monitor passes the captured data to the parser.</span></span> <span data-ttu-id="93166-114">Данные передаются на основе экземпляра протокола.</span><span class="sxs-lookup"><span data-stu-id="93166-114">The data is passed on a protocol instance basis.</span></span>
2.  <span data-ttu-id="93166-115">Определите расположение свойства в экземпляре протокола.</span><span class="sxs-lookup"><span data-stu-id="93166-115">Determine the location of the property in the protocol instance.</span></span>
3.  <span data-ttu-id="93166-116">Присоедините определение свойства к расположению свойства.</span><span class="sxs-lookup"><span data-stu-id="93166-116">Attach a property definition to the property location.</span></span>

<span data-ttu-id="93166-117">Сетевой монитор реализует структуру [**пропертинст**](propertyinst.md) , когда средство синтаксического анализа использует данные свойства в том виде, в котором оно существует в записи.</span><span class="sxs-lookup"><span data-stu-id="93166-117">Network Monitor implements a [**PROPERTYINST**](propertyinst.md) structure when the parser uses the property data as it exists in the capture.</span></span> <span data-ttu-id="93166-118">Сетевой монитор реализует структуру [**пропертинстекс**](propertyinstex.md) , когда синтаксический анализатор должен изменить данные свойства в записи.</span><span class="sxs-lookup"><span data-stu-id="93166-118">Network Monitor implements a [**PROPERTYINSTEX**](propertyinstex.md) structure when the parser must modify the property data in the capture.</span></span>

 

 



