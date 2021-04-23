---
title: атрибут code
description: Атрибут \ Code \ ACF вызывает создание кода клиентской заглушки для удаленных функций.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- атрибут кода MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334667"
---
# <a name="code-attribute"></a><span data-ttu-id="66df2-104">атрибут code</span><span class="sxs-lookup"><span data-stu-id="66df2-104">code attribute</span></span>

<span data-ttu-id="66df2-105">Атрибут **\[ Code \]** ACF вызывает создание кода клиентской заглушки для удаленных функций.</span><span class="sxs-lookup"><span data-stu-id="66df2-105">The **\[code\]** ACF attribute causes client stub code to be generated for remote functions.</span></span>

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="66df2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66df2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66df2-107">*Атрибуты ACF-Interface-*</span><span class="sxs-lookup"><span data-stu-id="66df2-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-108">Указывает список из одного или нескольких атрибутов, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="66df2-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="66df2-109">Допустимые атрибуты включают либо [**\[ автоматическую \_ обработку \]**](auto-handle.md) , либо [**\[ неявный \_ \] маркер**](implicit-handle.md) , а также **\[ код \]**, [**\[ некод \]**](nocode.md)или [**\[ оптимизацию \]**](optimize.md).</span><span class="sxs-lookup"><span data-stu-id="66df2-109">Valid attributes include either [**\[auto\_handle\]**](auto-handle.md) or [**\[implicit\_handle\]**](implicit-handle.md) and either **\[code\]**, [**\[nocode\]**](nocode.md), or [**\[optimize\]**](optimize.md).</span></span> <span data-ttu-id="66df2-110">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="66df2-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="66df2-111">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="66df2-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-112">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="66df2-112">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="66df2-113">*список имен файлов*</span><span class="sxs-lookup"><span data-stu-id="66df2-113">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-114">Указывает список из одного или нескольких имен файлов заголовка C, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="66df2-114">Specifies a list of one or more C-header file names, separated by commas.</span></span> <span data-ttu-id="66df2-115">Необходимо указать полное имя файла, включая расширение.</span><span class="sxs-lookup"><span data-stu-id="66df2-115">You must supply the full file name, including the extension.</span></span>

</dd> <dt>

<span data-ttu-id="66df2-116">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="66df2-116">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-117">Задает список из одного или нескольких атрибутов, разделенных запятыми, которые применяются к указанному типу.</span><span class="sxs-lookup"><span data-stu-id="66df2-117">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="66df2-118">Допустимые атрибуты типа включают [**\[ выделение \]**](allocate.md) и [**\[ представление \_ в виде \]**](represent-as.md).</span><span class="sxs-lookup"><span data-stu-id="66df2-118">Valid type attributes include [**\[allocate\]**](allocate.md) and [**\[represent\_as\]**](represent-as.md).</span></span>

</dd> <dt>

<span data-ttu-id="66df2-119">*имени*</span><span class="sxs-lookup"><span data-stu-id="66df2-119">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-120">Указывает тип, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="66df2-120">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="66df2-121">Атрибуты типа в ACF могут применяться только к типам, ранее определенным в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="66df2-121">Type attributes in the ACF can be applied only to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="66df2-122">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="66df2-122">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-123">Указывает ноль или более атрибутов, применяемых к функции в целом, например [**\[ \_ состояние \]**](comm-status.md)связи.</span><span class="sxs-lookup"><span data-stu-id="66df2-123">Specifies zero or more attributes that apply to the function as a whole, such as [**\[comm\_status\]**](comm-status.md).</span></span> <span data-ttu-id="66df2-124">Атрибуты функции заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="66df2-124">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="66df2-125">Несколько атрибутов функции разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="66df2-125">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="66df2-126">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="66df2-126">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-127">Указывает имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="66df2-127">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="66df2-128">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="66df2-128">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-129">Указывает атрибуты ACF, которые применяются к параметру.</span><span class="sxs-lookup"><span data-stu-id="66df2-129">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="66df2-130">Обратите внимание, что к параметру можно применить ноль, один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="66df2-130">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="66df2-131">Несколько атрибутов параметров разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="66df2-131">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="66df2-132">Атрибуты параметра ACF заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="66df2-132">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="66df2-133">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="66df2-133">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="66df2-134">Задает параметр функции, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="66df2-134">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="66df2-135">Каждый параметр функции должен быть указан в той же последовательности и с тем же именем, что и в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="66df2-135">Each parameter for the function must be specified in the same sequence and with the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66df2-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66df2-136">Remarks</span></span>

<span data-ttu-id="66df2-137">Атрибут **\[ Code \]** может присутствовать в заголовке ACF или применяться к отдельной функции.</span><span class="sxs-lookup"><span data-stu-id="66df2-137">The **\[code\]** attribute can appear in the ACF header or be applied to an individual function.</span></span>

<span data-ttu-id="66df2-138">Когда атрибут **\[ Code \]** отображается в заголовке ACF, клиентский код заглушки создается для всех удаленных функций, которые не имеют атрибута функции с [**\[ кодом \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="66df2-138">When the **\[code\]** attribute appears in the ACF header, client stub code is generated for all remote functions that do not have the [**\[nocode\]**](nocode.md) function attribute.</span></span> <span data-ttu-id="66df2-139">Вы можете переопределить атрибут **\[ Code \]** в заголовке для отдельной функции, указав атрибут «без **\[ кода \]** » в качестве атрибута функции.</span><span class="sxs-lookup"><span data-stu-id="66df2-139">You can override the **\[code\]** attribute in the header for an individual function by specifying the **\[nocode\]** attribute as a function attribute.</span></span>

<span data-ttu-id="66df2-140">Если атрибут **\[ Code \]** присутствует в списке атрибутов удаленной функции, код клиентской заглушки создается для функции.</span><span class="sxs-lookup"><span data-stu-id="66df2-140">When the **\[code\]** attribute appears in the remote function's attribute list, client stub code is generated for the function.</span></span> <span data-ttu-id="66df2-141">Код заглушки клиента не создается, если:</span><span class="sxs-lookup"><span data-stu-id="66df2-141">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="66df2-142">Заголовок ACF [**\[ \] содержит атрибут InAttribute**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="66df2-142">The ACF header includes the [**\[nocode\]**](nocode.md) attribute.</span></span>
-   <span data-ttu-id="66df2-143">К функции применяется атрибут «без [**\[ кода \]**](nocode.md) ».</span><span class="sxs-lookup"><span data-stu-id="66df2-143">The [**\[nocode\]**](nocode.md) attribute is applied to the function.</span></span>
-   <span data-ttu-id="66df2-144">[**\[ Локальный \]**](local.md) атрибут применяется к функции в файле интерфейса.</span><span class="sxs-lookup"><span data-stu-id="66df2-144">The [**\[local\]**](local.md) attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="66df2-145">В списке интерфейс или атрибут функции может присутствовать либо **\[ Code \]** [**\[ \] , либо код**](nocode.md) , но выбранный вами элемент может отображаться только один раз в списке.</span><span class="sxs-lookup"><span data-stu-id="66df2-145">Either **\[code\]** or [**\[nocode\]**](nocode.md) can appear in the interface or function attribute list, but the one you choose can appear only once in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="66df2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66df2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66df2-147">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="66df2-147">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="66df2-148">**allocate**</span><span class="sxs-lookup"><span data-stu-id="66df2-148">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="66df2-149">**Автоматическая \_ работа**</span><span class="sxs-lookup"><span data-stu-id="66df2-149">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="66df2-150">**\_состояние связи**</span><span class="sxs-lookup"><span data-stu-id="66df2-150">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="66df2-151">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="66df2-151">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="66df2-152">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="66df2-152">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="66df2-153">**nocode**</span><span class="sxs-lookup"><span data-stu-id="66df2-153">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="66df2-154">**увеличить**</span><span class="sxs-lookup"><span data-stu-id="66df2-154">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="66df2-155">**представлять \_ как**</span><span class="sxs-lookup"><span data-stu-id="66df2-155">**represent\_as**</span></span>](represent-as.md)
</dt> </dl>

 

 




