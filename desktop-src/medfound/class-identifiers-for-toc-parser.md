---
description: Следующие классы объявляются и связываются с идентификаторами классов (CLSID) в вмкодекдсп. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Идентификаторы классов для средства синтаксического анализа оглавлений (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673159"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a><span data-ttu-id="20f60-103">Идентификаторы классов для средства синтаксического анализа оглавления</span><span class="sxs-lookup"><span data-stu-id="20f60-103">Class Identifiers for Table of Contents Parser</span></span>

<span data-ttu-id="20f60-104">Следующие классы объявляются и связываются с идентификаторами классов (CLSID) в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="20f60-104">The following classes are declared and associated with class identifiers (CLSIDs) in wmcodecdsp.h.</span></span>



| <span data-ttu-id="20f60-105">Имя класса</span><span class="sxs-lookup"><span data-stu-id="20f60-105">Class name</span></span>       | <span data-ttu-id="20f60-106">Понятное имя объекта</span><span class="sxs-lookup"><span data-stu-id="20f60-106">Friendly object name</span></span> |
|------------------|----------------------|
| <span data-ttu-id="20f60-107">ктоцентри</span><span class="sxs-lookup"><span data-stu-id="20f60-107">CTocEntry</span></span>        | <span data-ttu-id="20f60-108">Запись ОГЛАВЛЕНИя</span><span class="sxs-lookup"><span data-stu-id="20f60-108">TOC Entry</span></span>            |
| <span data-ttu-id="20f60-109">ктоцентрилист</span><span class="sxs-lookup"><span data-stu-id="20f60-109">CTocEntryList</span></span>    | <span data-ttu-id="20f60-110">Список записей ОГЛАВЛЕНИя</span><span class="sxs-lookup"><span data-stu-id="20f60-110">TOC Entry List</span></span>       |
| <span data-ttu-id="20f60-111">кток</span><span class="sxs-lookup"><span data-stu-id="20f60-111">CToc</span></span>             | <span data-ttu-id="20f60-112">ОГЛАВЛЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20f60-112">TOC</span></span>                  |
| <span data-ttu-id="20f60-113">ктокколлектион</span><span class="sxs-lookup"><span data-stu-id="20f60-113">CTocCollection</span></span>   | <span data-ttu-id="20f60-114">Коллекция TOC</span><span class="sxs-lookup"><span data-stu-id="20f60-114">TOC Collection</span></span>       |
| <span data-ttu-id="20f60-115">ктокпарсер</span><span class="sxs-lookup"><span data-stu-id="20f60-115">CTocParser</span></span>       | <span data-ttu-id="20f60-116">Средство синтаксического анализа ОГЛАВЛЕНИя</span><span class="sxs-lookup"><span data-stu-id="20f60-116">TOC Parser</span></span>           |
| <span data-ttu-id="20f60-117">ктокженератордмо</span><span class="sxs-lookup"><span data-stu-id="20f60-117">CTocGeneratorDmo</span></span> | <span data-ttu-id="20f60-118">Генератор содержания</span><span class="sxs-lookup"><span data-stu-id="20f60-118">TOC Generator</span></span>        |



 

<span data-ttu-id="20f60-119">В приведенной выше таблице приводятся понятные имена объектов для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="20f60-119">The preceding table gives a friendly object name for each class.</span></span> <span data-ttu-id="20f60-120">В этой документации эти понятные имена используются для ссылки на экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="20f60-120">This documentation uses those friendly names to refer to instances of the classes.</span></span> <span data-ttu-id="20f60-121">Например, документация ссылается на экземпляр класса Ктоцентри в качестве объекта записи ОГЛАВЛЕНИя.</span><span class="sxs-lookup"><span data-stu-id="20f60-121">For example, the documentation refers to an instance of the CTocEntry class as a TOC Entry object.</span></span>

<span data-ttu-id="20f60-122">В коде можно использовать **\_ \_ ууидоф** для ссылки на идентификаторы CLSID.</span><span class="sxs-lookup"><span data-stu-id="20f60-122">In code, you can use **\_\_uuidof** to refer to the CLSIDs.</span></span> <span data-ttu-id="20f60-123">Например, можно использовать следующий код для ссылки на идентификатор CLSID для Ктокженератордмо.</span><span class="sxs-lookup"><span data-stu-id="20f60-123">For example, you can use the following code to refer to the CLSID for CTocGeneratorDmo.</span></span>


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a><span data-ttu-id="20f60-124">Константы CLSID, определенные в Вмкодекдсп. h</span><span class="sxs-lookup"><span data-stu-id="20f60-124">CLSID Constants Defined in Wmcodecdsp.h</span></span>

<span data-ttu-id="20f60-125">В качестве альтернативы использованию **\_ \_ ууидоф** можно использовать константы для ссылки на идентификаторы CLSID.</span><span class="sxs-lookup"><span data-stu-id="20f60-125">As an alternative to using **\_\_uuidof**, you can use constants to refer to the CLSIDs.</span></span> <span data-ttu-id="20f60-126">В вмкодекдсп. h определены следующие константы.</span><span class="sxs-lookup"><span data-stu-id="20f60-126">The following constants are defined in wmcodecdsp.h</span></span>



| <span data-ttu-id="20f60-127">Имя класса</span><span class="sxs-lookup"><span data-stu-id="20f60-127">Class name</span></span>     | <span data-ttu-id="20f60-128">Константа CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-128">CLSID constant</span></span>        |
|----------------|-----------------------|
| <span data-ttu-id="20f60-129">ктоцентри</span><span class="sxs-lookup"><span data-stu-id="20f60-129">CTocEntry</span></span>      | <span data-ttu-id="20f60-130">\_КТОЦЕНТРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-130">CLSID\_CTocEntry</span></span>      |
| <span data-ttu-id="20f60-131">ктоцентрилист</span><span class="sxs-lookup"><span data-stu-id="20f60-131">CTocEntryList</span></span>  | <span data-ttu-id="20f60-132">\_КТОЦЕНТРИЛИСТ CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-132">CLSID\_CTocEntryList</span></span>  |
| <span data-ttu-id="20f60-133">кток</span><span class="sxs-lookup"><span data-stu-id="20f60-133">CToc</span></span>           | <span data-ttu-id="20f60-134">\_КТОК CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-134">CLSID\_CToc</span></span>           |
| <span data-ttu-id="20f60-135">ктокколлектион</span><span class="sxs-lookup"><span data-stu-id="20f60-135">CTocCollection</span></span> | <span data-ttu-id="20f60-136">\_КТОККОЛЛЕКТИОН CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-136">CLSID\_CTocCollection</span></span> |
| <span data-ttu-id="20f60-137">ктокпарсер</span><span class="sxs-lookup"><span data-stu-id="20f60-137">CTocParser</span></span>     | <span data-ttu-id="20f60-138">\_КТОКПАРСЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-138">CLSID\_CTocParser</span></span>     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a><span data-ttu-id="20f60-139">Константы CLSID, определенные в Вмкодекдспууид. lib</span><span class="sxs-lookup"><span data-stu-id="20f60-139">CLSID Constants Defined in Wmcodecdspuuid.lib</span></span>

<span data-ttu-id="20f60-140">Следующая константа CLSID объявлена, но не определена в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="20f60-140">The following CLSID constant is declared, but not defined, in wmcodecdsp.h.</span></span> <span data-ttu-id="20f60-141">Чтобы использовать его в коде, необходимо выполнить компоновку к вмкодекдспууид. lib.</span><span class="sxs-lookup"><span data-stu-id="20f60-141">To use it in code, you must link against wmcodecdspuuid.lib.</span></span>



| <span data-ttu-id="20f60-142">Имя класса</span><span class="sxs-lookup"><span data-stu-id="20f60-142">Class name</span></span>       | <span data-ttu-id="20f60-143">Константа CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-143">CLSID constant</span></span>          |
|------------------|-------------------------|
| <span data-ttu-id="20f60-144">ктокженератордмо</span><span class="sxs-lookup"><span data-stu-id="20f60-144">CTocGeneratorDmo</span></span> | <span data-ttu-id="20f60-145">\_КТОКЖЕНЕРАТОРДМО CLSID</span><span class="sxs-lookup"><span data-stu-id="20f60-145">CLSID\_CTocGeneratorDmo</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="20f60-146">Требования</span><span class="sxs-lookup"><span data-stu-id="20f60-146">Requirements</span></span>



| <span data-ttu-id="20f60-147">Требование</span><span class="sxs-lookup"><span data-stu-id="20f60-147">Requirement</span></span> | <span data-ttu-id="20f60-148">Значение</span><span class="sxs-lookup"><span data-stu-id="20f60-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20f60-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20f60-149">Minimum supported client</span></span><br/> | <span data-ttu-id="20f60-150">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20f60-150">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="20f60-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20f60-151">Minimum supported server</span></span><br/> | <span data-ttu-id="20f60-152">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20f60-152">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20f60-153">Header</span><span class="sxs-lookup"><span data-stu-id="20f60-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="20f60-154"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f60-154"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="20f60-155">DLL</span><span class="sxs-lookup"><span data-stu-id="20f60-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20f60-156"><dt>Wmvdspa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20f60-156"><dt>Wmvdspa.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="20f60-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20f60-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f60-158">Таблица объектов средства синтаксического анализа содержимого</span><span class="sxs-lookup"><span data-stu-id="20f60-158">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> </dl>

 

 




