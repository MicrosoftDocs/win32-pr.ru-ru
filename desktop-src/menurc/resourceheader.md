---
title: Структура РЕСАУРЦЕХЕАДЕР
description: Содержит сведения о самом заголовке ресурса и данных, относящихся к этому ресурсу.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Меню структуры РЕСАУРЦЕХЕАДЕР и другие ресурсы
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710460"
---
# <a name="resourceheader-structure"></a><span data-ttu-id="2d549-104">Структура РЕСАУРЦЕХЕАДЕР</span><span class="sxs-lookup"><span data-stu-id="2d549-104">RESOURCEHEADER structure</span></span>

<span data-ttu-id="2d549-105">Содержит сведения о самом заголовке ресурса и данных, относящихся к этому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2d549-105">Contains information about the resource header itself and the data specific to this resource.</span></span> <span data-ttu-id="2d549-106">Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины.</span><span class="sxs-lookup"><span data-stu-id="2d549-106">This structure is not a true C-language structure, because it contains variable-length members.</span></span> <span data-ttu-id="2d549-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="2d549-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d549-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d549-108">Syntax</span></span>


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a><span data-ttu-id="2d549-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2d549-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2d549-110">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="2d549-110">**DataSize**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d549-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-112">Размер данных в байтах, которые следуют за заголовком ресурса для этого конкретного ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d549-112">The size, in bytes, of the data that follows the resource header for this particular resource.</span></span> <span data-ttu-id="2d549-113">Он не включает в файл ресурсов заполнение файлов между этим ресурсом и любым ресурсом, который следует за ним.</span><span class="sxs-lookup"><span data-stu-id="2d549-113">It does not include any file padding between this resource and any resource that follows it in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="2d549-114">**хеадерсизе**</span><span class="sxs-lookup"><span data-stu-id="2d549-114">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-115">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d549-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-116">Размер данных заголовка ресурса в байтах, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="2d549-116">The size, in bytes, of the resource header data that follows.</span></span>

</dd> <dt>

<span data-ttu-id="2d549-117">**TYPE**</span><span class="sxs-lookup"><span data-stu-id="2d549-117">**TYPE**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-118">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d549-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-119">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d549-119">The resource type.</span></span> <span data-ttu-id="2d549-120">Членом **типа** может быть либо числовое значение, либо строка в Юникоде, заканчивающаяся нулем, которая указывает имя типа.</span><span class="sxs-lookup"><span data-stu-id="2d549-120">The **TYPE** member can either be a numeric value or a null-terminated Unicode string that specifies the name of the type.</span></span> <span data-ttu-id="2d549-121">Описание элементов **имени** или **порядкового** типа см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="2d549-121">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="2d549-122">Если член **типа** является числовым значением, он может указать либо стандартный, либо определяемый пользователем тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d549-122">If the **TYPE** member is a numeric value, it can specify either a standard or a user-defined resource type.</span></span> <span data-ttu-id="2d549-123">Если элемент является строкой, то это определяемый пользователем тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d549-123">If the member is a string, then it is a user-defined resource type.</span></span> <span data-ttu-id="2d549-124">Список предопределенных типов ресурсов см. в разделе [типы ресурсов](/windows/desktop/menurc/resource-types).</span><span class="sxs-lookup"><span data-stu-id="2d549-124">For a list of the predefined resource types, see [Resource Types](/windows/desktop/menurc/resource-types).</span></span>

<span data-ttu-id="2d549-125">Значения меньше 256 зарезервированы для использования системой.</span><span class="sxs-lookup"><span data-stu-id="2d549-125">Values less than 256 are reserved for system use.</span></span>

</dd> <dt>

<span data-ttu-id="2d549-126">**ИМЯ**</span><span class="sxs-lookup"><span data-stu-id="2d549-126">**NAME**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-127">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d549-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-128">Имя, идентифицирующее конкретный ресурс.</span><span class="sxs-lookup"><span data-stu-id="2d549-128">A name that identifies the particular resource.</span></span> <span data-ttu-id="2d549-129">Элемент **Name** , как и член **типа** , может быть числовым значением или строкой Юникода, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="2d549-129">The **NAME** member, like the **TYPE** member, can either be a numeric value or a null-terminated Unicode string.</span></span> <span data-ttu-id="2d549-130">Описание элементов **имени** или **порядкового** типа см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="2d549-130">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="2d549-131">Нет необходимости добавлять заполнение для выравнивания **DWORD** между членами **типа** и **имени** , так как они содержат данные **Word** .</span><span class="sxs-lookup"><span data-stu-id="2d549-131">You do not need to add padding for **DWORD** alignment between the **TYPE** and **NAME** members because they contain **WORD** data.</span></span> <span data-ttu-id="2d549-132">Однако может потребоваться добавить **слово** заполнения после элемента **Name** , чтобы вычислить остальную часть заголовка на границах **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2d549-132">However, you may need to add a **WORD** of padding after the **NAME** member to align the rest of the header on **DWORD** boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="2d549-133">**Версия**</span><span class="sxs-lookup"><span data-stu-id="2d549-133">**DataVersion**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-134">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d549-134">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-135">Предопределенная версия данных ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d549-135">A predefined resource data version.</span></span> <span data-ttu-id="2d549-136">Это определит версию данных ресурса, которую должно использовать приложение.</span><span class="sxs-lookup"><span data-stu-id="2d549-136">This will determine which version of the resource data the application should use.</span></span>

</dd> <dt>

<span data-ttu-id="2d549-137">**меморифлагс**</span><span class="sxs-lookup"><span data-stu-id="2d549-137">**MemoryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-138">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="2d549-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-139">Набор флагов атрибутов, которые могут описывать состояние ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d549-139">A set of attribute flags that can describe the state of the resource.</span></span> <span data-ttu-id="2d549-140">Модификаторы в. Файл скрипта RC назначает ресурсу эти атрибуты.</span><span class="sxs-lookup"><span data-stu-id="2d549-140">Modifiers in the .RC script file assign these attributes to the resource.</span></span> <span data-ttu-id="2d549-141">Идентификаторы сценариев могут назначать следующие значения флагов.</span><span class="sxs-lookup"><span data-stu-id="2d549-141">The script identifiers can assign the following flag values.</span></span>

<span data-ttu-id="2d549-142">Приложения не используют ни один из этих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2d549-142">Applications do not use any of these attributes.</span></span> <span data-ttu-id="2d549-143">В скрипте разрешены атрибуты для обратной совместимости с существующими скриптами, но они игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2d549-143">The attributes are permitted in the script for backward compatibility with existing scripts, but they are ignored.</span></span> <span data-ttu-id="2d549-144">Ресурсы загружаются при загрузке соответствующего модуля и освобождаются при выгрузке модуля.</span><span class="sxs-lookup"><span data-stu-id="2d549-144">Resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

<span data-ttu-id="2d549-145">**Перемещаемая** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="2d549-145">**MOVEABLE** (0x0010)</span></span>


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

<span data-ttu-id="2d549-146">**Исправлено** (~ перемещаемое)</span><span class="sxs-lookup"><span data-stu-id="2d549-146">**FIXED** (~MOVEABLE)</span></span>


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

<span data-ttu-id="2d549-147">**Чистый** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="2d549-147">**PURE** (0x0020)</span></span>


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

<span data-ttu-id="2d549-148">**НЕчистое** (~ чистое)</span><span class="sxs-lookup"><span data-stu-id="2d549-148">**IMPURE** (~PURE)</span></span>


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

<span data-ttu-id="2d549-149">**Предварительная загрузка** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="2d549-149">**PRELOAD** (0x0040)</span></span>


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

<span data-ttu-id="2d549-150">**лоадонкалл** (~ Предварительная загрузка)</span><span class="sxs-lookup"><span data-stu-id="2d549-150">**LOADONCALL** (~PRELOAD)</span></span>


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

<span data-ttu-id="2d549-151">**Отклонено** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="2d549-151">**DISCARDABLE** (0x1000)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="2d549-152">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="2d549-152">**LanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-153">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="2d549-153">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-154">Язык ресурса или набора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d549-154">The language for the resource or set of resources.</span></span> <span data-ttu-id="2d549-155">Задайте значение для этого элемента с помощью необязательной инструкции определения [языкового](./language-statement.md) ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d549-155">Set the value for this member with the optional [LANGUAGE](./language-statement.md) resource definition statement.</span></span> <span data-ttu-id="2d549-156">Параметры являются константами из файла Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="2d549-156">The parameters are constants from the Winnt.h file.</span></span>

<span data-ttu-id="2d549-157">Каждый ресурс включает идентификатор языка, поэтому система или приложение могут выбрать язык, подходящий для текущего языкового стандарта системы.</span><span class="sxs-lookup"><span data-stu-id="2d549-157">Each resource includes a language identifier so the system or application can select a language appropriate for the current locale of the system.</span></span> <span data-ttu-id="2d549-158">При наличии нескольких ресурсов одного типа и имени, отличающихся только языком строк внутри ресурсов, необходимо указать **LanguageId** для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="2d549-158">If there are multiple resources of the same type and name that differ only in the language of the strings within the resources, you will need to specify a **LanguageId** for each one.</span></span>

</dd> <dt>

<span data-ttu-id="2d549-159">**Version**</span><span class="sxs-lookup"><span data-stu-id="2d549-159">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-160">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d549-160">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-161">Определяемый пользователем номер версии для данных ресурсов, которые средства могут использовать для чтения и записи файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d549-161">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span> <span data-ttu-id="2d549-162">Задайте это значение с помощью необязательной инструкции определения ресурса [версии](./version-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="2d549-162">Set this value with the optional [VERSION](./version-statement.md) resource definition statement.</span></span>

</dd> <dt>

<span data-ttu-id="2d549-163">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="2d549-163">**Characteristics**</span></span>
</dt> <dd>

<span data-ttu-id="2d549-164">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d549-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2d549-165">Указывает определяемую пользователем информацию о ресурсе, который средства могут использовать для чтения и записи файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d549-165">Specifies user-defined information about the resource that tools can use to read and write resource files.</span></span> <span data-ttu-id="2d549-166">Задайте это значение с помощью инструкции определения ресурса необязательных [характеристик](./characteristics-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="2d549-166">Set this value with the optional [CHARACTERISTICS](./characteristics-statement.md) resource definition statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d549-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d549-167">Remarks</span></span>

<span data-ttu-id="2d549-168">Член типа переменной называется членом **имени** или **порядкового номера** и используется в большинстве мест в файле ресурсов, где отображается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2d549-168">A variable type member is called a **Name** or **Ordinal** member, and it is used in most places in the resource file where an identifier appears.</span></span> <span data-ttu-id="2d549-169">Первое **слово** элемента типа **Name** или **Ordinal** указывает, является ли элемент числовым значением или строкой.</span><span class="sxs-lookup"><span data-stu-id="2d549-169">The first **WORD** of a **Name** or **Ordinal** type member indicates whether the member is a numeric value or a string.</span></span> <span data-ttu-id="2d549-170">Если первое **слово** в члене равно значению 0xFFFF, которое является недопустимым символом Юникода, следующее **слово** является числом типа.</span><span class="sxs-lookup"><span data-stu-id="2d549-170">If the first **WORD** in the member is equal to the value 0xffff, which is an invalid Unicode character, then the following **WORD** is a type number.</span></span> <span data-ttu-id="2d549-171">В противном случае элемент содержит строку в Юникоде, а первое **слово** в члене — первый символ в строке имени.</span><span class="sxs-lookup"><span data-stu-id="2d549-171">Otherwise, the member contains a Unicode string and the first **WORD** in the member is the first character in the name string.</span></span> <span data-ttu-id="2d549-172">Дополнительные сведения об инструкциях определения ресурсов см. в разделе [инструкции определения ресурсов](./resource-definition-statements.md).</span><span class="sxs-lookup"><span data-stu-id="2d549-172">For additional information about resource definition statements, see [Resource-Definition Statements](./resource-definition-statements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d549-173">Требования</span><span class="sxs-lookup"><span data-stu-id="2d549-173">Requirements</span></span>



| <span data-ttu-id="2d549-174">Требование</span><span class="sxs-lookup"><span data-stu-id="2d549-174">Requirement</span></span> | <span data-ttu-id="2d549-175">Значение</span><span class="sxs-lookup"><span data-stu-id="2d549-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2d549-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d549-176">Minimum supported client</span></span><br/> | <span data-ttu-id="2d549-177">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d549-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2d549-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d549-178">Minimum supported server</span></span><br/> | <span data-ttu-id="2d549-179">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d549-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2d549-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d549-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d549-181">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2d549-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2d549-182">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="2d549-182">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="2d549-183">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="2d549-183">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2d549-184">Оператор характеристик</span><span class="sxs-lookup"><span data-stu-id="2d549-184">CHARACTERISTICS Statement</span></span>](./characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="2d549-185">LANGUAGE, инструкция</span><span class="sxs-lookup"><span data-stu-id="2d549-185">LANGUAGE Statement</span></span>](./language-statement.md)
</dt> <dt>

[<span data-ttu-id="2d549-186">VERSION, инструкция</span><span class="sxs-lookup"><span data-stu-id="2d549-186">VERSION Statement</span></span>](./version-statement.md)
</dt> </dl>

 

