---
title: атрибут "без кода"
description: Атрибут \ InAttribute \ используется в заголовках ACF или с отдельными функциями для предотвращения создания кода клиентской заглушки.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- атрибут некодека MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333576"
---
# <a name="nocode-attribute"></a><span data-ttu-id="e3594-104">атрибут "без кода"</span><span class="sxs-lookup"><span data-stu-id="e3594-104">nocode attribute</span></span>

<span data-ttu-id="e3594-105">Атрибут InAttribute используется в заголовках ACF или с отдельными функциями для предотвращения создания кода клиентской заглушки. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="e3594-105">The **\[nocode\]** attribute is used in ACF headers or with individual functions to prevent the generation of client stub code.</span></span>

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="e3594-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3594-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3594-107">*Атрибуты ACF-Interface-*</span><span class="sxs-lookup"><span data-stu-id="e3594-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-108">Указывает список из одного или нескольких атрибутов, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="e3594-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="e3594-109">Допустимые атрибуты включают в себя либо **\[** [**автоматическую \_ обработку**](auto-handle.md) **\]** , либо **\[** [**неявный \_**](implicit-handle.md) **\]** **\[** [](code.md) **\]** **\[ \]** маркер, либо код или код.</span><span class="sxs-lookup"><span data-stu-id="e3594-109">Valid attributes include either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]** and either **\[**[**code**](code.md)**\]** or **\[nocode\]**.</span></span> <span data-ttu-id="e3594-110">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="e3594-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-111">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="e3594-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-112">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e3594-112">Specifies the name of the interface.</span></span> <span data-ttu-id="e3594-113">В режиме совместимости с DCE имя интерфейса должно совпадать с именем интерфейса, указанного в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e3594-113">In DCE-compatibility mode, the interface name must match the name of the interface specified in the IDL file.</span></span> <span data-ttu-id="e3594-114">При использовании параметра компилятора MIDL [**/АКФ**](-acf.md)имя интерфейса в ACF и имя интерфейса в IDL-файле могут отличаться.</span><span class="sxs-lookup"><span data-stu-id="e3594-114">When you use the MIDL compiler switch [**/acf**](-acf.md), the interface name in the ACF and the interface name in the IDL file can be different.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-115">*список имен файлов*</span><span class="sxs-lookup"><span data-stu-id="e3594-115">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-116">Указывает список из одного или нескольких имен файлов заголовков языка C, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="e3594-116">Specifies a list of one or more C-language header file names, separated by commas.</span></span> <span data-ttu-id="e3594-117">Необходимо указать полное имя файла, включая расширение.</span><span class="sxs-lookup"><span data-stu-id="e3594-117">The full file name, including the extension, must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-118">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e3594-118">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-119">Задает список из одного или нескольких атрибутов, разделенных запятыми, которые применяются к указанному типу.</span><span class="sxs-lookup"><span data-stu-id="e3594-119">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="e3594-120">Допустимые атрибуты типа включают **\[** [**выделение**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e3594-120">Valid type attributes include **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-121">*имени*</span><span class="sxs-lookup"><span data-stu-id="e3594-121">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-122">Указывает тип, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e3594-122">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="e3594-123">Атрибуты типа в ACF могут применяться только к типам, ранее определенным в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e3594-123">Type attributes in the ACF can only be applied to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-124">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="e3594-124">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-125">Задает атрибуты, применяемые к функции в целом, например **\[** [**\_ состояние**](comm-status.md)связи **\]** .</span><span class="sxs-lookup"><span data-stu-id="e3594-125">Specifies attributes that apply to the function as a whole, such as **\[**[**comm\_status**](comm-status.md)**\]**.</span></span> <span data-ttu-id="e3594-126">Атрибуты функции заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="e3594-126">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="e3594-127">Несколько атрибутов функции разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="e3594-127">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-128">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="e3594-128">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-129">Указывает имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e3594-129">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-130">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="e3594-130">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-131">Указывает атрибуты ACF, которые применяются к параметру.</span><span class="sxs-lookup"><span data-stu-id="e3594-131">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="e3594-132">Обратите внимание, что к параметру можно применить ноль или более атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e3594-132">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="e3594-133">Несколько атрибутов параметров разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="e3594-133">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="e3594-134">Атрибуты параметра ACF заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="e3594-134">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="e3594-135">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="e3594-135">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3594-136">Задает параметр функции, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e3594-136">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="e3594-137">Каждый параметр функции должен быть указан в одной и той же последовательности и использовать те же имена, что и в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e3594-137">Each parameter for the function must be specified in the same sequence and using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3594-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3594-138">Remarks</span></span>

<span data-ttu-id="e3594-139">Атрибут InAttribute может присутствовать в заголовке ACF, или его можно применить к отдельной функции. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="e3594-139">The **\[nocode\]** attribute can appear in the ACF header, or it can be applied to an individual function.</span></span>

<span data-ttu-id="e3594-140">Если атрибут InAttribute присутствует в заголовке ACF, клиентский код заглушки не создается для какой-либо удаленной функции, если он не имеет атрибута функции Code **. \[ \]** **\[** [](code.md) **\]**</span><span class="sxs-lookup"><span data-stu-id="e3594-140">When the **\[nocode\]** attribute appears in the ACF header, client stub code is not generated for any remote function unless it has the **\[**[**code**](code.md)**\]** function attribute.</span></span> <span data-ttu-id="e3594-141">Можно **\[ \] переопределить атрибут** кода в заголовке для отдельной функции, указав атрибут **\[ Code \]** в качестве атрибута функции.</span><span class="sxs-lookup"><span data-stu-id="e3594-141">You can override the **\[nocode\]** attribute in the header for an individual function by specifying the **\[code\]** attribute as a function attribute.</span></span>

<span data-ttu-id="e3594-142">Если атрибут " **\[ некод \]** " присутствует в списке атрибутов функции, код клиентской заглушки для функции не создается.</span><span class="sxs-lookup"><span data-stu-id="e3594-142">When the **\[nocode\]** attribute appears in the function's attribute list, no client stub code is generated for the function.</span></span>

<span data-ttu-id="e3594-143">Код заглушки клиента не создается, если:</span><span class="sxs-lookup"><span data-stu-id="e3594-143">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="e3594-144">Заголовок ACF **\[ \] содержит атрибут InAttribute** .</span><span class="sxs-lookup"><span data-stu-id="e3594-144">The ACF header includes the **\[nocode\]** attribute.</span></span>
-   <span data-ttu-id="e3594-145">К функции применяется атрибут «без **\[ кода \]** ».</span><span class="sxs-lookup"><span data-stu-id="e3594-145">The **\[nocode\]** attribute is applied to the function.</span></span>
-   <span data-ttu-id="e3594-146">**\[** [**Локальный**](local.md) **\]** атрибут применяется к функции в файле интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e3594-146">The **\[**[**local**](local.md)**\]** attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="e3594-147">**\[** [](code.md) **\]** В списке атрибутов **\[ \]** функции может присутствовать либо код, либо код ".</span><span class="sxs-lookup"><span data-stu-id="e3594-147">Either **\[**[**code**](code.md)**\]** or **\[nocode\]** can appear in a function's attribute list, and the one you choose can appear exactly once.</span></span>

<span data-ttu-id="e3594-148">При создании заглушек сервера атрибут с **\[ кодом \]** не учитывается.</span><span class="sxs-lookup"><span data-stu-id="e3594-148">The **\[nocode\]** attribute is ignored when server stubs are generated.</span></span> <span data-ttu-id="e3594-149">Его нельзя применить при создании заглушек сервера в режиме совместимости с DCE.</span><span class="sxs-lookup"><span data-stu-id="e3594-149">You cannot apply it when generating server stubs in DCE-compatibility mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3594-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3594-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3594-151">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="e3594-151">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="e3594-152">**/акф**</span><span class="sxs-lookup"><span data-stu-id="e3594-152">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="e3594-153">**allocate**</span><span class="sxs-lookup"><span data-stu-id="e3594-153">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="e3594-154">**Автоматическая \_ работа**</span><span class="sxs-lookup"><span data-stu-id="e3594-154">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="e3594-155">**приведен**</span><span class="sxs-lookup"><span data-stu-id="e3594-155">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="e3594-156">**\_состояние связи**</span><span class="sxs-lookup"><span data-stu-id="e3594-156">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="e3594-157">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="e3594-157">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> </dl>

 

 




