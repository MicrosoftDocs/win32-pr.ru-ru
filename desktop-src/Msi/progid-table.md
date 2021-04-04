---
description: Таблица ProgId содержит сведения о идентификаторах программ и идентификаторах программ независимых версий, которые должны быть созданы как часть объявления продукта.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Таблица ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999518"
---
# <a name="progid-table"></a><span data-ttu-id="9d812-103">Таблица ProgId</span><span class="sxs-lookup"><span data-stu-id="9d812-103">ProgId Table</span></span>

<span data-ttu-id="9d812-104">Таблица ProgId содержит сведения о идентификаторах программ и идентификаторах программ независимых версий, которые должны быть созданы как часть объявления продукта.</span><span class="sxs-lookup"><span data-stu-id="9d812-104">The ProgId table contains information for program IDs and version independent program IDs that must be generated as a part of the product advertisement.</span></span>

<span data-ttu-id="9d812-105">Таблица ProgId содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="9d812-105">The ProgId table has the following columns.</span></span>



| <span data-ttu-id="9d812-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="9d812-106">Column</span></span>         | <span data-ttu-id="9d812-107">Type</span><span class="sxs-lookup"><span data-stu-id="9d812-107">Type</span></span>                         | <span data-ttu-id="9d812-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="9d812-108">Key</span></span> | <span data-ttu-id="9d812-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="9d812-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="9d812-110">ProgId</span><span class="sxs-lookup"><span data-stu-id="9d812-110">ProgId</span></span>         | [<span data-ttu-id="9d812-111">Text</span><span class="sxs-lookup"><span data-stu-id="9d812-111">Text</span></span>](text.md)             | <span data-ttu-id="9d812-112">Да</span><span class="sxs-lookup"><span data-stu-id="9d812-112">Y</span></span>   | <span data-ttu-id="9d812-113">Нет</span><span class="sxs-lookup"><span data-stu-id="9d812-113">N</span></span>        |
| <span data-ttu-id="9d812-114">\_Родительский объект ProgID</span><span class="sxs-lookup"><span data-stu-id="9d812-114">ProgId\_Parent</span></span> | [<span data-ttu-id="9d812-115">Text</span><span class="sxs-lookup"><span data-stu-id="9d812-115">Text</span></span>](text.md)             | <span data-ttu-id="9d812-116">Нет</span><span class="sxs-lookup"><span data-stu-id="9d812-116">N</span></span>   | <span data-ttu-id="9d812-117">Да</span><span class="sxs-lookup"><span data-stu-id="9d812-117">Y</span></span>        |
| <span data-ttu-id="9d812-118">Класс\_</span><span class="sxs-lookup"><span data-stu-id="9d812-118">Class\_</span></span>        | [<span data-ttu-id="9d812-119">GUID</span><span class="sxs-lookup"><span data-stu-id="9d812-119">GUID</span></span>](guid.md)             | <span data-ttu-id="9d812-120">Нет</span><span class="sxs-lookup"><span data-stu-id="9d812-120">N</span></span>   | <span data-ttu-id="9d812-121">Да</span><span class="sxs-lookup"><span data-stu-id="9d812-121">Y</span></span>        |
| <span data-ttu-id="9d812-122">Описание</span><span class="sxs-lookup"><span data-stu-id="9d812-122">Description</span></span>    | [<span data-ttu-id="9d812-123">Text</span><span class="sxs-lookup"><span data-stu-id="9d812-123">Text</span></span>](text.md)             | <span data-ttu-id="9d812-124">Нет</span><span class="sxs-lookup"><span data-stu-id="9d812-124">N</span></span>   | <span data-ttu-id="9d812-125">Да</span><span class="sxs-lookup"><span data-stu-id="9d812-125">Y</span></span>        |
| <span data-ttu-id="9d812-126">Значок\_</span><span class="sxs-lookup"><span data-stu-id="9d812-126">Icon\_</span></span>         | [<span data-ttu-id="9d812-127">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="9d812-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="9d812-128">Нет</span><span class="sxs-lookup"><span data-stu-id="9d812-128">N</span></span>   | <span data-ttu-id="9d812-129">Да</span><span class="sxs-lookup"><span data-stu-id="9d812-129">Y</span></span>        |
| <span data-ttu-id="9d812-130">икониндекс</span><span class="sxs-lookup"><span data-stu-id="9d812-130">IconIndex</span></span>      | [<span data-ttu-id="9d812-131">Integer</span><span class="sxs-lookup"><span data-stu-id="9d812-131">Integer</span></span>](integer.md)       | <span data-ttu-id="9d812-132">Нет</span><span class="sxs-lookup"><span data-stu-id="9d812-132">N</span></span>   | <span data-ttu-id="9d812-133">Да</span><span class="sxs-lookup"><span data-stu-id="9d812-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9d812-134">Столбцы</span><span class="sxs-lookup"><span data-stu-id="9d812-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9d812-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ID</span><span class="sxs-lookup"><span data-stu-id="9d812-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span></span>
</dt> <dd>

<span data-ttu-id="9d812-136">Идентификатор программы или независимый от версии код программы.</span><span class="sxs-lookup"><span data-stu-id="9d812-136">The program ID or version independent program ID.</span></span> <span data-ttu-id="9d812-137">Идентификаторы ProgId, перечисленные в таблице ProgId, регистрируются, если для класса CLSID, указанного в \_ столбце Class этой таблицы, запланировано объявление или установка.</span><span class="sxs-lookup"><span data-stu-id="9d812-137">ProgIds listed in the ProgId table are registered if the CLSID listed in the Class\_column of this table is scheduled to be advertised or installed.</span></span> <span data-ttu-id="9d812-138">При выборе ProgId для регистрации все идентификаторы ProgId, ссылающиеся на эту строку через \_ родительский столбец ProgID, также выбираются для регистрации.</span><span class="sxs-lookup"><span data-stu-id="9d812-138">When the ProgId is selected for registration, all ProgIds that refer to this row through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="9d812-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>\_Родительский объект ProgID</span><span class="sxs-lookup"><span data-stu-id="9d812-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="9d812-140">Определен только для идентификаторов программы, независимых от версии.</span><span class="sxs-lookup"><span data-stu-id="9d812-140">Defined only for version independent program IDs.</span></span> <span data-ttu-id="9d812-141">Это поле является внешним ключом в столбце ProgId.</span><span class="sxs-lookup"><span data-stu-id="9d812-141">This field is a foreign key into the ProgId column.</span></span> <span data-ttu-id="9d812-142">Чтобы определить идентификатор программы независимо от версии, введите соответствующий идентификатор ProgId в \_ родительский столбец ProgID.</span><span class="sxs-lookup"><span data-stu-id="9d812-142">To define a version independent program ID, enter the corresponding ProgId into the ProgId\_Parent column.</span></span> <span data-ttu-id="9d812-143">Если для установки выбран идентификатор ProgId, то для регистрации также выбираются соответствующие независимые от версии идентификаторы ProgId, связанные через \_ родительский столбец ProgID.</span><span class="sxs-lookup"><span data-stu-id="9d812-143">When the ProgId is selected for installation, the corresponding version-independent ProgIds associated through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="9d812-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="9d812-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Class\_</span></span>
</dt> <dd>

<span data-ttu-id="9d812-145">Необязательный внешний ключ в [таблице классов](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="9d812-145">An optional foreign key into the [Class table](class-table.md).</span></span> <span data-ttu-id="9d812-146">Этот столбец должен иметь значение NULL для независимого от версии идентификатора ProgId.</span><span class="sxs-lookup"><span data-stu-id="9d812-146">This column must be Null for a version independent ProgId.</span></span> <span data-ttu-id="9d812-147">Если значение класса \_ ProgID равно null, идентификатор ProgID регистрируется в том случае, если он отображается в столбце ProgID строки в [таблице расширений](extension-table.md) , а расширение содержит по крайней мере одну команду, связанную с ней в [таблице команд](verb-table.md).</span><span class="sxs-lookup"><span data-stu-id="9d812-147">If the Class\_value for a ProgId is null, the ProgId is registered when it appears in the ProgId column of a row in the [Extension table](extension-table.md) and the extension has at least one Verb associated with it in the [Verb table](verb-table.md).</span></span> <span data-ttu-id="9d812-148">Идентификаторы ProgId, выбранные для регистрации таким способом, не устанавливают другие идентификаторы ProgId, которые ссылаются на текущий идентификатор ProgId, с помощью \_ значения ProgID по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9d812-148">ProgIds selected for registration in this manner do not install other ProgIds that reference the current ProgId through the ProgId\_Default value.</span></span>

</dd> <dt>

<span data-ttu-id="9d812-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="9d812-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="9d812-150">Необязательное локализованное описание идентификатора связанной программы.</span><span class="sxs-lookup"><span data-stu-id="9d812-150">An optional localized description of the associated program ID.</span></span>

</dd> <dt>

<span data-ttu-id="9d812-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Значок\_</span><span class="sxs-lookup"><span data-stu-id="9d812-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="9d812-152">Необязательный внешний ключ в [таблице значков](icon-table.md) , указывающий файл значка, связанный с этим ProgID.</span><span class="sxs-lookup"><span data-stu-id="9d812-152">An optional foreign key into the [Icon table](icon-table.md) that specifies the icon file associated with this ProgId.</span></span> <span data-ttu-id="9d812-153">Это написано с помощью ключа Дефаултикон, связанного с этим ProgId.</span><span class="sxs-lookup"><span data-stu-id="9d812-153">This is written under the DefaultIcon key associated with this ProgId.</span></span> <span data-ttu-id="9d812-154">Этот столбец должен иметь значение NULL для независимого от версии идентификатора ProgId.</span><span class="sxs-lookup"><span data-stu-id="9d812-154">This column must be Null for a version independent ProgId.</span></span>

</dd> <dt>

<span data-ttu-id="9d812-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>икониндекс</span><span class="sxs-lookup"><span data-stu-id="9d812-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="9d812-156">Индекс значка в файле значка.</span><span class="sxs-lookup"><span data-stu-id="9d812-156">The Icon index into the icon file.</span></span> <span data-ttu-id="9d812-157">Этот столбец должен иметь значение NULL для независимого от версии идентификатора ProgId.</span><span class="sxs-lookup"><span data-stu-id="9d812-157">This column must be Null for a version independent ProgId.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d812-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d812-158">Remarks</span></span>

<span data-ttu-id="9d812-159">Действия [регистерпрогидинфо](registerprogidinfo-action.md) и [унрегистерпрогидинфо](unregisterprogidinfo-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="9d812-159">The [RegisterProgIdInfo](registerprogidinfo-action.md) and [UnregisterProgIdInfo](unregisterprogidinfo-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="9d812-160">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9d812-160">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="9d812-161">Проверка</span><span class="sxs-lookup"><span data-stu-id="9d812-161">Validation</span></span>

<dl>

[<span data-ttu-id="9d812-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="9d812-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9d812-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="9d812-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9d812-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="9d812-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9d812-165">ICE36</span><span class="sxs-lookup"><span data-stu-id="9d812-165">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="9d812-166">ICE89</span><span class="sxs-lookup"><span data-stu-id="9d812-166">ICE89</span></span>](ice89.md)  
</dl>

 

 



