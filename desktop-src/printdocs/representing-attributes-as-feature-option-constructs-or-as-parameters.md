---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Представление атрибутов в виде конструкций "функция-параметр" или "Параметры"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104081738"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="2e10e-104">Представление атрибутов в виде конструкций "функция-параметр" или "Параметры"</span><span class="sxs-lookup"><span data-stu-id="2e10e-104">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="2e10e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2e10e-105">This topic is not current.</span></span> <span data-ttu-id="2e10e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2e10e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2e10e-107">Автор документа PrintCapabilities определяет атрибуты устройства, которые составляют конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2e10e-107">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="2e10e-108">В документе PrintCapabilities автор может представить атрибут устройства как конструкцию функции или варианта или как конструкцию параметра.</span><span class="sxs-lookup"><span data-stu-id="2e10e-108">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="2e10e-109">Если атрибут устройства имеет относительно небольшое число возможных состояний, не относящихся ни к одному из очевидных шаблонов, то лучше выбрать конструкцию "функция-параметр".</span><span class="sxs-lookup"><span data-stu-id="2e10e-109">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="2e10e-110">Например, если допустимыми значениями для атрибута устройства Пажемедиасизе являются значения Letter, Legal, A4ISO, tabloid и Envelope10, то для представления лучше выбрать конструкцию "функция-параметр".</span><span class="sxs-lookup"><span data-stu-id="2e10e-110">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="2e10e-111">Из-за сложности и неоднозначности, связанной с выражением допустимых значений без явного перечисления, конструкция параметра не подходит для атрибута Пажемедиасизе.</span><span class="sxs-lookup"><span data-stu-id="2e10e-111">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="2e10e-112">Если атрибут устройства может быть представлен диапазоном целых чисел, лучше выбрать представление параметра, особенно для диапазонов, включающих множество значений.</span><span class="sxs-lookup"><span data-stu-id="2e10e-112">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="2e10e-113">Например, если атрибут устройства Копикаунт для конкретной модели принтера может находиться в диапазоне от 1 до 99 999, то этот атрибут следует классифицировать как параметр, определив экземпляр Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="2e10e-113">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="2e10e-114">Назначьте значения для экземпляров свойств MinValue и MaxValue элемента Параметердеф, чтобы определить диапазон значений для атрибута Жобкопикаунт.</span><span class="sxs-lookup"><span data-stu-id="2e10e-114">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="2e10e-115">Из-за большого количества значений, которые должны быть явно перечислены как элементы параметров, представление "функция/параметр" не подходит для атрибута устройства Жобкопикаунт.</span><span class="sxs-lookup"><span data-stu-id="2e10e-115">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e10e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="2e10e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e10e-117">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2e10e-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



