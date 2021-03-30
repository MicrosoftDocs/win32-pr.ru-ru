---
description: Квалификатор ключа указывает, является ли свойство частью обработчика пространства имен.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Квалификатор ключа
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816121"
---
# <a name="key-qualifier"></a><span data-ttu-id="60bcd-103">Квалификатор ключа</span><span class="sxs-lookup"><span data-stu-id="60bcd-103">Key Qualifier</span></span>

<span data-ttu-id="60bcd-104">Квалификатор **ключа** указывает, является ли свойство частью обработчика пространства имен.</span><span class="sxs-lookup"><span data-stu-id="60bcd-104">The **Key** qualifier indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="60bcd-105">Если квалификатор **ключа** имеется в нескольких свойствах, то все эти свойства вместе формируют ключ (составной ключ).</span><span class="sxs-lookup"><span data-stu-id="60bcd-105">If more than one property has the **Key** qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="60bcd-106">При совместном использовании ключевые свойства должны предоставлять уникальную ссылку на каждый экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="60bcd-106">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="60bcd-107">Если этот квалификатор размещается в свойстве, то допускается только значение **true** .</span><span class="sxs-lookup"><span data-stu-id="60bcd-107">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

<span data-ttu-id="60bcd-108">Можно использовать любой тип свойства, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="60bcd-108">You can use any property type except for the following:</span></span>

-   <span data-ttu-id="60bcd-109">Массивы</span><span class="sxs-lookup"><span data-stu-id="60bcd-109">Arrays</span></span>
-   <span data-ttu-id="60bcd-110">Вещественное число и числа с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="60bcd-110">Real and floating-point numbers</span></span>
-   <span data-ttu-id="60bcd-111">Внедренные объекты</span><span class="sxs-lookup"><span data-stu-id="60bcd-111">Embedded objects</span></span>
-   <span data-ttu-id="60bcd-112">Символы меньше, чем ASCII 32 (то есть символы пробела)</span><span class="sxs-lookup"><span data-stu-id="60bcd-112">Characters lower than ASCII 32 (that is, white space characters)</span></span>
-   <span data-ttu-id="60bcd-113">Символьные строки типа **Char16** или символьные строки, определенные как ключи, должны содержать значения, превышающие U + 0020.</span><span class="sxs-lookup"><span data-stu-id="60bcd-113">Character strings of type **char16** or character strings that are defined as keys must contain values greater than U+0020.</span></span> <span data-ttu-id="60bcd-114">Это обусловлено тем, что WMI использует значения ключа в путях объектов, и нельзя использовать непечатаемые символы в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="60bcd-114">This is because WMI uses key values in object paths, and you cannot use nonprinting characters in an object path.</span></span>

<span data-ttu-id="60bcd-115">Если родительский класс задает ключ, все классы, производные от родительского класса, наследуют этот ключ.</span><span class="sxs-lookup"><span data-stu-id="60bcd-115">When a parent class specifies a key, all classes derived from the parent class inherit that key.</span></span> <span data-ttu-id="60bcd-116">Производные классы не могут изменять наследуемый ключ или определять любое новое ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="60bcd-116">The derived classes cannot alter the inherited key or define any new key property.</span></span> <span data-ttu-id="60bcd-117">Однако при наследовании подкласса от абстрактного класса без ключа можно ввести ключ в подкласс.</span><span class="sxs-lookup"><span data-stu-id="60bcd-117">However, when you derive a subclass from an abstract class without a key, you can introduce a key in the subclass.</span></span>

<span data-ttu-id="60bcd-118">Все классы, определяющие более одного экземпляра, должны указывать ключ.</span><span class="sxs-lookup"><span data-stu-id="60bcd-118">All classes that define more than one instance must specify a key.</span></span> <span data-ttu-id="60bcd-119">Поскольку абстрактные классы не определяют какие-либо экземпляры, им не нужно указывать ключи.</span><span class="sxs-lookup"><span data-stu-id="60bcd-119">Because abstract classes do not define any instances, they do not need to specify keys.</span></span> <span data-ttu-id="60bcd-120">Поскольку Одноэлементные классы определяют только один экземпляр, они не могут указывать ключи.</span><span class="sxs-lookup"><span data-stu-id="60bcd-120">Because singleton classes define only one instance, they cannot specify keys.</span></span>

<span data-ttu-id="60bcd-121">Ключи записываются один раз при создании экземпляра объекта и не должны изменяться позже.</span><span class="sxs-lookup"><span data-stu-id="60bcd-121">Keys are written one time at object instantiation and must not be modified later.</span></span> <span data-ttu-id="60bcd-122">Не имеет смысла применять значение по умолчанию к свойству с указанием ключа.</span><span class="sxs-lookup"><span data-stu-id="60bcd-122">It does not make sense to apply a default value to a key-qualified property.</span></span>

## <a name="requirements"></a><span data-ttu-id="60bcd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="60bcd-123">Requirements</span></span>



| <span data-ttu-id="60bcd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="60bcd-124">Requirement</span></span> | <span data-ttu-id="60bcd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="60bcd-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="60bcd-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60bcd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="60bcd-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60bcd-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="60bcd-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60bcd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="60bcd-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60bcd-129">Windows Server 2008</span></span><br/> |



 

 




