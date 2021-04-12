---
title: Объединения RPC
description: Инкапсулированные и неинкапсулированные объединения и их формат с помощью удаленного вызова процедур (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487744"
---
# <a name="rpc-unions"></a><span data-ttu-id="990a5-103">Объединения RPC</span><span class="sxs-lookup"><span data-stu-id="990a5-103">RPC unions</span></span>

<span data-ttu-id="990a5-104">Как инкапсулированные, так и неинкапсулированные объединения имеют общий \_ \_ селектор<> :</span><span class="sxs-lookup"><span data-stu-id="990a5-104">Both encapsulated and nonencapsulated unions share a common union\_arm\_selector<> format:</span></span>

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

<span data-ttu-id="990a5-105">Поле Union \_ подлокотники<2> состоит из двух частей.</span><span class="sxs-lookup"><span data-stu-id="990a5-105">The union\_arms<2> field consists of two parts.</span></span> <span data-ttu-id="990a5-106">Если объединение является объединением в стиле MIDL 1,0, верхние 4 бита содержат выравнивание линии объединения (выравнивание с наибольшим выровненным ARM).</span><span class="sxs-lookup"><span data-stu-id="990a5-106">If the union is a MIDL 1.0 style union, the upper 4 bits contain the alignment of the union arm (alignment of greatest aligned arm).</span></span> <span data-ttu-id="990a5-107">В противном случае верхние 4 бита равны нулю.</span><span class="sxs-lookup"><span data-stu-id="990a5-107">Otherwise the upper 4 bits are zero.</span></span> <span data-ttu-id="990a5-108">Младшие 12 битов содержат число подлокотников в объединении.</span><span class="sxs-lookup"><span data-stu-id="990a5-108">The lower 12 bits contain the number of arms in the union.</span></span> <span data-ttu-id="990a5-109">Другими словами:</span><span class="sxs-lookup"><span data-stu-id="990a5-109">In other words:</span></span>

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

<span data-ttu-id="990a5-110">Смещение \_ для \_ описания ARM \_<2> поля содержат относительное смещение со знаком для описания типа ARM.</span><span class="sxs-lookup"><span data-stu-id="990a5-110">The offset\_to\_arm\_description<2> fields contain a relative signed offset to the arm's type description.</span></span> <span data-ttu-id="990a5-111">Однако поле перегружается с оптимизацией для простых типов.</span><span class="sxs-lookup"><span data-stu-id="990a5-111">However, the field is overloaded with optimization for simple types.</span></span> <span data-ttu-id="990a5-112">Для этого смещение в верхнем байте этого поля смещения составляет FC \_ Magic \_ Union \_ Byte (0x80), а нижний байт короткого формата — фактический тип символа для ARM.</span><span class="sxs-lookup"><span data-stu-id="990a5-112">For these, the upper byte of this offset field is FC\_MAGIC\_UNION\_BYTE (0x80) and the lower byte of the short is the actual format character type of the arm.</span></span> <span data-ttu-id="990a5-113">Таким образом, для значений смещения существует два диапазона: "80 *XX*" означает, что *XX* является строкой формата типа; и все остальное в диапазоне (80 FF.</span><span class="sxs-lookup"><span data-stu-id="990a5-113">As such, there are two ranges for the offset values: "80 *xx*" means that *xx* is a type format string; and everything else within range (80 FF ..</span></span> <span data-ttu-id="990a5-114">7F FF) означает фактическое смещение.</span><span class="sxs-lookup"><span data-stu-id="990a5-114">7f FF) means an actual offset.</span></span> <span data-ttu-id="990a5-115">Это делает смещение от диапазона <80 00..</span><span class="sxs-lookup"><span data-stu-id="990a5-115">This makes offsets from range <80 00 ..</span></span> <span data-ttu-id="990a5-116">80 FF > недоступен в качестве смещений.</span><span class="sxs-lookup"><span data-stu-id="990a5-116">80 FF > unavailable as offsets.</span></span> <span data-ttu-id="990a5-117">Компилятор проверяет, что версия MIDL 5.1.164.</span><span class="sxs-lookup"><span data-stu-id="990a5-117">The compiler checks that as of MIDL version 5.1.164.</span></span>

<span data-ttu-id="990a5-118">В \_ поле Описание ARM по умолчанию \_<2>а указывает тип ARM объединения для ARM по умолчанию (при наличии).</span><span class="sxs-lookup"><span data-stu-id="990a5-118">The default\_arm\_description<2> field indicates the type of union arm for the default arm, if any.</span></span> <span data-ttu-id="990a5-119">Если для объединения не указана ARM по умолчанию, описание ARM по умолчанию \_ \_<2> поле имеет значение 0xFFFF, и возникает исключение, если параметр не \_ соответствует ни одному из значений варианта ARM.</span><span class="sxs-lookup"><span data-stu-id="990a5-119">If there is no default arm specified for the union then the default\_arm\_description<2> field is 0xFFFF and an exception is raised if the switch\_is value does not match any of the arm case values.</span></span> <span data-ttu-id="990a5-120">Если значение ARM по умолчанию указано, но пусто, то описание ARM по умолчанию \_ \_<2> поле равно нулю.</span><span class="sxs-lookup"><span data-stu-id="990a5-120">If the default arm is specified but empty, then the default\_arm\_description<2> field is zero.</span></span> <span data-ttu-id="990a5-121">В противном случае в \_ описании ARM по умолчанию \_<2> поле имеет ту же семантику, что и смещение \_ к \_ \_ описанию ARM<2> поля.</span><span class="sxs-lookup"><span data-stu-id="990a5-121">Otherwise the default\_arm\_description<2> field has the same semantics as the offset\_to\_arm\_description<2> fields.</span></span>

<span data-ttu-id="990a5-122">Ниже приведено краткое описание.</span><span class="sxs-lookup"><span data-stu-id="990a5-122">The following is a summary:</span></span>

-   <span data-ttu-id="990a5-123">0 — пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="990a5-123">0 - empty default</span></span>
-   <span data-ttu-id="990a5-124">FFFF — нет значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="990a5-124">FFFF - no default</span></span>
-   <span data-ttu-id="990a5-125">80xx — простой тип</span><span class="sxs-lookup"><span data-stu-id="990a5-125">80xx - simple type</span></span>
-   <span data-ttu-id="990a5-126">другое относительное смещение</span><span class="sxs-lookup"><span data-stu-id="990a5-126">other - relative offset</span></span>

## <a name="encapsulated-unions"></a><span data-ttu-id="990a5-127">Инкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="990a5-127">Encapsulated Unions</span></span>

<span data-ttu-id="990a5-128">Инкапсулированное объединение поступает из специального синтаксиса UNION в IDL.</span><span class="sxs-lookup"><span data-stu-id="990a5-128">An encapsulated union comes from a special union syntax in IDL.</span></span> <span data-ttu-id="990a5-129">Фактически инкапсулированное объединение — это структура пакета с полем discriminant в начале структуры, а объединение — единственным другим элементом.</span><span class="sxs-lookup"><span data-stu-id="990a5-129">Effectively, an encapsulated union is a bundle structure with a discriminant field at the beginning of the structure and the union as the only other member.</span></span>

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

<span data-ttu-id="990a5-130">Тип переключателя инкапсулированного объединения \_<1> поле состоит из двух частей.</span><span class="sxs-lookup"><span data-stu-id="990a5-130">An encapsulated union's switch\_type<1> field has two parts.</span></span> <span data-ttu-id="990a5-131">В нижней части содержится фактический тип переключателя, а верхняя часть — это величина, на которую необходимо увеличить указатель памяти, чтобы пропустить переход за пределы \_ поля Switch, которое включает в себя любое заполнение между полем Switch — \_ () структуры, сформированной заглушкой, и фактическим полем объединения.</span><span class="sxs-lookup"><span data-stu-id="990a5-131">The lower nibble provides the actual switch type, and the upper nibble provides the memory increment to step over that is an amount that the memory pointer must be incremented to skip past the switch\_is field, which includes any padding between the switch\_is() field of the stub-constructed structure and the actual union field.</span></span>

<span data-ttu-id="990a5-132">Размер памяти \_<2> поле имеет размер только для объединения и идентичен неинкапсулированным объединениям.</span><span class="sxs-lookup"><span data-stu-id="990a5-132">The memory\_size<2> field is the size of the union only, and is identical to nonencapsulated unions.</span></span> <span data-ttu-id="990a5-133">Чтобы получить общий размер структуры, содержащей объединение, добавьте объем памяти \_<2> в шаг с обходом по шагам, то есть верхнюю часть типа переключателя \_<1> поле, а затем выровняйте по выравниванию, соответствующему инкременту.</span><span class="sxs-lookup"><span data-stu-id="990a5-133">To obtain the total size of the structure that contains the union, add memory\_size<2> to memory increment to step over, that is to the upper nibble of the switch\_type<1> field, then align by the alignment corresponding to the increment.</span></span>

## <a name="nonencapsulated-unions"></a><span data-ttu-id="990a5-134">Неинкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="990a5-134">Nonencapsulated Unions</span></span>

<span data-ttu-id="990a5-135">Неинкапсулированное объединение — типичная ситуация, когда объединение является одним аргументом или полем, а параметр — другим аргументом или полем соответственно.</span><span class="sxs-lookup"><span data-stu-id="990a5-135">A nonencapsulated union is a typical situation where a union is one argument or field and the switch is another argument or field, respectively.</span></span>

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

<span data-ttu-id="990a5-136">Где:</span><span class="sxs-lookup"><span data-stu-id="990a5-136">Where:</span></span>

<span data-ttu-id="990a5-137">Тип переключателя \_<1> поле является символом формата для discriminant.</span><span class="sxs-lookup"><span data-stu-id="990a5-137">The switch\_type<1> field is a format character for the discriminant.</span></span>

<span data-ttu-id="990a5-138">Параметр \_ является \_ дескриптором<> поле является дескриптором корреляции и имеет 4 или 6 байт в зависимости от того, используется ли [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="990a5-138">The switch\_is\_descriptor<> field is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="990a5-139">Однако для параметра \_ \_ Description<>, если объединение внедрено в структуру, Поле Offset параметра \_ имеет значение Description, \_<> является смещением переключателя \_ от позиции объединения в структуре (а не от начала структуры).</span><span class="sxs-lookup"><span data-stu-id="990a5-139">However, for the switch\_is\_description<>, if the union is embedded in a structure, the offset field of the switch\_is\_description<> is the offset to the switch\_is field from the union's position in the structure (not from the beginning of the structure).</span></span>

<span data-ttu-id="990a5-140">Смещение \_ к \_ размеру \_ и \_ описание ARM \_<2> поле дает смещение для размера объединения и описания ARM, которые идентичны для инкапсулированных объединений и являются общими для всех неинкапсулированных объединений того же типа:</span><span class="sxs-lookup"><span data-stu-id="990a5-140">The offset\_to\_size\_and\_arm\_description<2> field gives the offset to the union's size and arm description, which is identical to that for encapsulated unions and is shared by all nonencapsulated unions of the same type :</span></span>

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 