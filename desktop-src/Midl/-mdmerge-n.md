---
title: параметр/n
description: Параметр/n указывает глубину композиции для создания файлов метаданных.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n переключить MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689246"
---
# <a name="n-switch"></a><span data-ttu-id="7d664-104">параметр/n</span><span class="sxs-lookup"><span data-stu-id="7d664-104">/n switch</span></span>

<span data-ttu-id="7d664-105">Параметр **/n** указывает глубину композиции для создания файлов метаданных.</span><span class="sxs-lookup"><span data-stu-id="7d664-105">The **/n** switch specifies the composition depth for composing metadata files.</span></span>

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a><span data-ttu-id="7d664-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="7d664-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="7d664-107">*Глубина пространства имен \_*</span><span class="sxs-lookup"><span data-stu-id="7d664-107">*namespace\_depth*</span></span> 
</dt> <dd>

<span data-ttu-id="7d664-108">Указывает глубину пространства имен, которая должна быть составляться в один файл метаданных.</span><span class="sxs-lookup"><span data-stu-id="7d664-108">Specifies the namespace depth to compose into a single metadata file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d664-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d664-109">Remarks</span></span>

<span data-ttu-id="7d664-110">Ниже приведены возможные форматы значений, которые можно указать с помощью параметра **/n** .</span><span class="sxs-lookup"><span data-stu-id="7d664-110">Here are the possible value formats that you can specify with the **/n** switch.</span></span>



| <span data-ttu-id="7d664-111">Формат значения</span><span class="sxs-lookup"><span data-stu-id="7d664-111">Value format</span></span>                   | <span data-ttu-id="7d664-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7d664-112">Description</span></span>                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7d664-113">Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="7d664-113">Int32 > 0</span></span>                   | <span data-ttu-id="7d664-114">Сформируйте все типы на глубине пространства имен, указанной в параметре.</span><span class="sxs-lookup"><span data-stu-id="7d664-114">Compose all types at the namespace depth specified in the switch.</span></span>               |
| <span data-ttu-id="7d664-115">-1</span><span class="sxs-lookup"><span data-stu-id="7d664-115">-1</span></span>                             | <span data-ttu-id="7d664-116">Составьте все типы в один IDL-файл на пространство имен.</span><span class="sxs-lookup"><span data-stu-id="7d664-116">Compose all types into one IDL file per namespace.</span></span>                              |
| <span data-ttu-id="7d664-117"><namespace>: Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="7d664-117"><namespace>:Int32 > 0</span></span> | <span data-ttu-id="7d664-118">Составьте все типы с совпадающим пространством имен на глубине, указанной в параметре.</span><span class="sxs-lookup"><span data-stu-id="7d664-118">Compose all types with matching namespace at the depth specified in the switch.</span></span> |
| <span data-ttu-id="7d664-119"><namespace>:-1</span><span class="sxs-lookup"><span data-stu-id="7d664-119"><namespace>:-1</span></span>           | <span data-ttu-id="7d664-120">Составьте все типы с совпадающим пространством имен в один файл для каждого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7d664-120">Compose all types with matching namespace into one file per namespace.</span></span>          |



 

<span data-ttu-id="7d664-121">В следующей таблице показаны результаты различных сочетаний ключа **/n** , работающих над этими пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="7d664-121">The following table shows the results from different combinations of the **/n** switch working on these namespaces.</span></span>

-   <span data-ttu-id="7d664-122">Windows. Foundation. Collections. Иитерабле</span><span class="sxs-lookup"><span data-stu-id="7d664-122">Windows.Foundation.Collections.IIterable</span></span>
-   <span data-ttu-id="7d664-123">Windows. UI. Директуи. Controls. Button</span><span class="sxs-lookup"><span data-stu-id="7d664-123">Windows.UI.DirectUI.Controls.Button</span></span>
-   <span data-ttu-id="7d664-124">Windows. UI. Директуи. Controls. ListView</span><span class="sxs-lookup"><span data-stu-id="7d664-124">Windows.UI.DirectUI.Controls.ListView</span></span>
-   <span data-ttu-id="7d664-125">Windows. UI. иммерсивное. Application. Плайто. Target</span><span class="sxs-lookup"><span data-stu-id="7d664-125">Windows.UI.Immersive.Application.PlayTo.Target</span></span>
-   <span data-ttu-id="7d664-126">Windows. Web. синдикации. RSS</span><span class="sxs-lookup"><span data-stu-id="7d664-126">Windows.Web.Syndication.RSS</span></span>



| <span data-ttu-id="7d664-127">коммутаторы;</span><span class="sxs-lookup"><span data-stu-id="7d664-127">Switches</span></span>                         | <span data-ttu-id="7d664-128">Результат</span><span class="sxs-lookup"><span data-stu-id="7d664-128">Result</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="7d664-129">Объяснение</span><span class="sxs-lookup"><span data-stu-id="7d664-129">Explanation</span></span>                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d664-130">**/n:-1**  / **n:1**</span><span class="sxs-lookup"><span data-stu-id="7d664-130">**/n:-1** /**n:1**</span></span>               | <span data-ttu-id="7d664-131">Windows.winmd</span><span class="sxs-lookup"><span data-stu-id="7d664-131">Windows.winmd</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="7d664-132">Последний параметр/n переопределяет все предыдущие параметры – n.</span><span class="sxs-lookup"><span data-stu-id="7d664-132">The last /n switch overrides all previous –n switches.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7d664-133">**/n:-1/n: Windows. UI: 2**</span><span class="sxs-lookup"><span data-stu-id="7d664-133">**/n:-1/n:Windows.UI:2**</span></span>         | <dl> <span data-ttu-id="7d664-134">Windows <dt>. Foundation. winmd</dt> Windows. <dt>UI. winmd</dt> , <dt>Windows. Web.</dt> WinMD</span><span class="sxs-lookup"><span data-stu-id="7d664-134"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.winmd</dt> <dt>Windows.Web.Syndication.winmd</dt></span></span> </dl> | <dl> <span data-ttu-id="7d664-135"><dt>**Windows. Foundation** всегда состоит из – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="7d664-135"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="7d664-136"><dt>Типы **Windows. UI** сгруппированы.</dt></span><span class="sxs-lookup"><span data-stu-id="7d664-136"><dt>**Windows.UI** types are grouped.</dt></span></span> <span data-ttu-id="7d664-137"><dt>**Windows. Web. синдикации** состоит из n:-1.</dt></span><span class="sxs-lookup"><span data-stu-id="7d664-137"><dt>**Windows.Web.Syndication** is composed at n:-1.</dt></span></span> </dl>       |
| <span data-ttu-id="7d664-138">**/n: 1/n: Windows. UI. Директуи: 3**</span><span class="sxs-lookup"><span data-stu-id="7d664-138">**/n:1/n:Windows.UI.DirectUI:3**</span></span> | <dl> <span data-ttu-id="7d664-139">Windows <dt>. Foundation. winmd</dt> <dt>Windows. UI. директуи. winmd</dt> <dt>Windows. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="7d664-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span></span> </dl>       | <dl> <span data-ttu-id="7d664-140"><dt>**Windows. Foundation** всегда состоит из – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="7d664-140"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="7d664-141"><dt>**Windows. UI. директуи** состоит на уровне 3.</dt></span><span class="sxs-lookup"><span data-stu-id="7d664-141"><dt>**Windows.UI.DirectUI** is composed at level 3.</dt></span></span> <span data-ttu-id="7d664-142"><dt>Все остальные типы состоят на уровне 1.</dt></span><span class="sxs-lookup"><span data-stu-id="7d664-142"><dt>All other types are composed at level 1.</dt></span></span> </dl> |



 

<span data-ttu-id="7d664-143">Ниже приведены правила обработки нескольких экземпляров параметра **/n** .</span><span class="sxs-lookup"><span data-stu-id="7d664-143">Here are the rules for handling multiple instances of the **/n** switch.</span></span>

-   <span data-ttu-id="7d664-144">Наиболее конкретный экземпляр имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="7d664-144">The most specific instance prevails.</span></span> <span data-ttu-id="7d664-145">Например, если указать **– н:а.б.к: 4 – н:а.б: 5**, мдмерже разрешает A. b. c. D на уровне 4, поскольку A. B. c является более конкретным, чем а.б.</span><span class="sxs-lookup"><span data-stu-id="7d664-145">For example, if you specify **–n:A.B.C:4–n:A.B:5**, MDMERGE resolves A.B.C.D at level 4, because A.B.C is more specific than A.B.</span></span> <span data-ttu-id="7d664-146">A. B. E. F разрешается глубиной 5, так как она соответствует A. B, но не А.Б.К.</span><span class="sxs-lookup"><span data-stu-id="7d664-146">A.B.E.F resolves at depth 5, because it matches A.B but not A.B.C.</span></span>
-   <span data-ttu-id="7d664-147">Последний экземпляр имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="7d664-147">The last instance prevails.</span></span> <span data-ttu-id="7d664-148">Например, если указать **– n:5 – n:2**, типы будут состоять на уровне 2.</span><span class="sxs-lookup"><span data-stu-id="7d664-148">For example, if you specify **–n:5–n:2**, the types are composed at level 2.</span></span>
-   <span data-ttu-id="7d664-149">Применяются оба правила.</span><span class="sxs-lookup"><span data-stu-id="7d664-149">Both of these rules apply.</span></span> <span data-ttu-id="7d664-150">Если указать – Н:а.б.к: 4 – Н:а.б.к: 1, пространство имен A. B. C будет состоять на уровне 1.</span><span class="sxs-lookup"><span data-stu-id="7d664-150">If you specify –n:A.B.C:4 –n:A.B.C:1, namespace A.B.C is composed at level 1.</span></span>

## <a name="examples"></a><span data-ttu-id="7d664-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="7d664-151">Examples</span></span>

<span data-ttu-id="7d664-152">**mdmerge.exe-Metadata \_ dir $ ( \_ путь метаданных пакета SDK \_ )-i $ ( \_ внутренний \_ путь метаданных SDK \_ )-o $ ( \_ путь к obj-файлу) \\ $O \\ SystemMetadata-v-n:-1-н:Виндовс.фаундатион: 2**</span><span class="sxs-lookup"><span data-stu-id="7d664-152">**mdmerge.exe -metadata\_dir $(SDK\_METADATA\_PATH) -i $(INTERNAL\_SDK\_METADATA\_PATH) -o $(OBJ\_PATH)\\$O\\SystemMetadata -v -n:-1 -n:Windows.Foundation:2**</span></span>

## <a name="requirements"></a><span data-ttu-id="7d664-153">Требования</span><span class="sxs-lookup"><span data-stu-id="7d664-153">Requirements</span></span>



| <span data-ttu-id="7d664-154">Требование</span><span class="sxs-lookup"><span data-stu-id="7d664-154">Requirement</span></span> | <span data-ttu-id="7d664-155">Значение</span><span class="sxs-lookup"><span data-stu-id="7d664-155">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="7d664-156">Клиент</span><span class="sxs-lookup"><span data-stu-id="7d664-156">Client</span></span><br/> | <span data-ttu-id="7d664-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7d664-157">Windows 8</span></span><br/>           |
| <span data-ttu-id="7d664-158">Сервер</span><span class="sxs-lookup"><span data-stu-id="7d664-158">Server</span></span><br/> | <span data-ttu-id="7d664-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d664-159">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d664-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d664-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d664-161">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="7d664-161">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





