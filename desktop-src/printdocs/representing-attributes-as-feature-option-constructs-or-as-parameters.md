---
description: Представляет атрибуты в качестве конструкций функций и параметров или в качестве параметров. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Представление атрибутов в виде конструкций "функция-параметр" или "Параметры"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120059"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="395ec-105">Представление атрибутов в виде конструкций "функция-параметр" или "Параметры"</span><span class="sxs-lookup"><span data-stu-id="395ec-105">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="395ec-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="395ec-106">This topic is not current.</span></span> <span data-ttu-id="395ec-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="395ec-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="395ec-108">Автор документа PrintCapabilities определяет атрибуты устройства, которые составляют конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="395ec-108">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="395ec-109">В документе PrintCapabilities автор может представить атрибут устройства как конструкцию функции или варианта или как конструкцию параметра.</span><span class="sxs-lookup"><span data-stu-id="395ec-109">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="395ec-110">Если атрибут устройства имеет относительно небольшое число возможных состояний, не относящихся ни к одному из очевидных шаблонов, то лучше выбрать конструкцию "функция-параметр".</span><span class="sxs-lookup"><span data-stu-id="395ec-110">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="395ec-111">Например, если допустимыми значениями для атрибута устройства Пажемедиасизе являются значения Letter, Legal, A4ISO, tabloid и Envelope10, то для представления лучше выбрать конструкцию "функция-параметр".</span><span class="sxs-lookup"><span data-stu-id="395ec-111">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="395ec-112">Из-за сложности и неоднозначности, связанной с выражением допустимых значений без явного перечисления, конструкция параметра не подходит для атрибута Пажемедиасизе.</span><span class="sxs-lookup"><span data-stu-id="395ec-112">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="395ec-113">Если атрибут устройства может быть представлен диапазоном целых чисел, лучше выбрать представление параметра, особенно для диапазонов, включающих множество значений.</span><span class="sxs-lookup"><span data-stu-id="395ec-113">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="395ec-114">Например, если атрибут устройства Копикаунт для конкретной модели принтера может находиться в диапазоне от 1 до 99 999, то этот атрибут следует классифицировать как параметр, определив экземпляр Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="395ec-114">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="395ec-115">Назначьте значения для экземпляров свойств MinValue и MaxValue элемента Параметердеф, чтобы определить диапазон значений для атрибута Жобкопикаунт.</span><span class="sxs-lookup"><span data-stu-id="395ec-115">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="395ec-116">Из-за большого количества значений, которые должны быть явно перечислены как элементы параметров, представление "функция/параметр" не подходит для атрибута устройства Жобкопикаунт.</span><span class="sxs-lookup"><span data-stu-id="395ec-116">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="395ec-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="395ec-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="395ec-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="395ec-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



