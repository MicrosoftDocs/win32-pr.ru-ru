---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Платформа для печати схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273306"
---
# <a name="print-schema-framework"></a><span data-ttu-id="2a67c-104">Платформа для печати схемы</span><span class="sxs-lookup"><span data-stu-id="2a67c-104">Print Schema Framework</span></span>

<span data-ttu-id="2a67c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2a67c-105">This topic is not current.</span></span> <span data-ttu-id="2a67c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2a67c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2a67c-107">В этом разделе содержатся более подробные сведения о значении и использовании типов элементов схемы печати.</span><span class="sxs-lookup"><span data-stu-id="2a67c-107">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="2a67c-108">Основной задачей первоначальной версии инфраструктуры печати схем является представление конфигураций и возможностей атрибутов устройств.</span><span class="sxs-lookup"><span data-stu-id="2a67c-108">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="2a67c-109">На высоком уровне эта платформа предлагает два различных стиля описания атрибута устройства: как конструкцию функции или варианта или как конструкцию параметра.</span><span class="sxs-lookup"><span data-stu-id="2a67c-109">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="2a67c-110">Если атрибут устройства имеет небольшое количество доступных значений или состояний, атрибут должен быть характеризуется как функция с допустимыми значениями или состояниями, называемыми элементами параметров.</span><span class="sxs-lookup"><span data-stu-id="2a67c-110">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="2a67c-111">И наоборот, если атрибут устройства имеет большое количество доступных значений или состояний, и набор всех возможных значений легко определить без необходимости явного перечисления, атрибут устройства должен быть выражен в виде параметра.</span><span class="sxs-lookup"><span data-stu-id="2a67c-111">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="2a67c-112">(Параметр определяется с помощью элемента Параметердеф, а экземпляр параметра инициализируется с помощью элемента Параметеринит.) Элементы свойств используются в конструкциях функций, параметров и параметров для обеспечения более точного уровня различий.</span><span class="sxs-lookup"><span data-stu-id="2a67c-112">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a67c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2a67c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a67c-114">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2a67c-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



