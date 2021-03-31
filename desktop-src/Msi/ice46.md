---
description: ICE46 проверяет наличие пользовательских свойств в условиях, форматированном тексте и других местах, которые отличаются от определяемого системой свойства только регистром одного или нескольких символов.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813321"
---
# <a name="ice46"></a><span data-ttu-id="7df05-103">ICE46</span><span class="sxs-lookup"><span data-stu-id="7df05-103">ICE46</span></span>

<span data-ttu-id="7df05-104">ICE46 проверяет наличие пользовательских свойств в условиях, форматированном тексте и других местах, которые отличаются от определяемого системой свойства только регистром одного или нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="7df05-104">ICE46 checks for custom properties in conditions, formatted text, and other locations that differ from a system defined property only by the case of one or more characters.</span></span>

## <a name="result"></a><span data-ttu-id="7df05-105">Результат</span><span class="sxs-lookup"><span data-stu-id="7df05-105">Result</span></span>

<span data-ttu-id="7df05-106">ICE46 отправляет информационное сообщение, если в условии, форматированном тексте имеется пользовательское свойство, а другое расположение отличается от свойств, заданных системой, только в случае одного или нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="7df05-106">ICE46 posts an informational message if there is a custom property in a condition, formatted text, and other location that differs from a system defined properties only in the case of one or more characters.</span></span>

## <a name="example"></a><span data-ttu-id="7df05-107">Пример</span><span class="sxs-lookup"><span data-stu-id="7df05-107">Example</span></span>

<span data-ttu-id="7df05-108">ICE46 сообщает о следующих ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="7df05-108">ICE46 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="7df05-109">ICE46, ошибка</span><span class="sxs-lookup"><span data-stu-id="7df05-109">ICE46 error</span></span>                                                                                                                                            | <span data-ttu-id="7df05-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7df05-110">Description</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df05-111">Свойство ReinstallMode, определенное в таблице свойств, отличается от другого определенного свойства только регистром.</span><span class="sxs-lookup"><span data-stu-id="7df05-111">Property ReinstallMode defined in property table differs from another defined property only by case.</span></span>                                                   | <span data-ttu-id="7df05-112">Имя свойства, определяемое системой **REINSTALLMODE** , отличается от пользовательского свойства только регистром.</span><span class="sxs-lookup"><span data-stu-id="7df05-112">The system defined property name **REINSTALLMODE** differs from the custom property by case only.</span></span> <span data-ttu-id="7df05-113">Свойства чувствительны к регистру, поэтому пользовательское свойство не совпадает с системным свойством.</span><span class="sxs-lookup"><span data-stu-id="7df05-113">Properties are case sensitive, so custom property is not the same as the system property.</span></span> <span data-ttu-id="7df05-114">Это распространенная причина ошибок.</span><span class="sxs-lookup"><span data-stu-id="7df05-114">This is a common cause of errors.</span></span> |
| <span data-ttu-id="7df05-115">Свойство "MyProperty", на которое имеется ссылка в столбце "Инсталлексекутесекуенце". Условие "строки" функции InstallFinalize "отличается от определенного свойства только регистром.</span><span class="sxs-lookup"><span data-stu-id="7df05-115">Property 'Myproperty' referenced in column 'InstallExecuteSequence'.'Condition' of row 'InstallFinalize' differs from a defined property by case only.</span></span> | <span data-ttu-id="7df05-116">Таблица свойств определяет таблицу MyProperty, но свойство, на которое указывает ссылка, имеет значение MyProperty.</span><span class="sxs-lookup"><span data-stu-id="7df05-116">The property table defines the table MyProperty, but the referenced property is Myproperty.</span></span> <span data-ttu-id="7df05-117">Свойства чувствительны к регистру, поэтому два свойства не совпадают.</span><span class="sxs-lookup"><span data-stu-id="7df05-117">Properties are case sensitive, so the two properties are NOT the same.</span></span> <span data-ttu-id="7df05-118">Это распространенная причина ошибок.</span><span class="sxs-lookup"><span data-stu-id="7df05-118">This is a common cause of errors.</span></span>                          |



 

[<span data-ttu-id="7df05-119">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="7df05-119">Property Table</span></span>](property-table.md)



| <span data-ttu-id="7df05-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="7df05-120">Property</span></span>      | <span data-ttu-id="7df05-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7df05-121">Value</span></span>   |
|---------------|---------|
| <span data-ttu-id="7df05-122">ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="7df05-122">ReinstallMode</span></span> | <span data-ttu-id="7df05-123">omus</span><span class="sxs-lookup"><span data-stu-id="7df05-123">omus</span></span>    |
| <span data-ttu-id="7df05-124">MyProperty</span><span class="sxs-lookup"><span data-stu-id="7df05-124">MyProperty</span></span>    | <span data-ttu-id="7df05-125">значение</span><span class="sxs-lookup"><span data-stu-id="7df05-125">a value</span></span> |



 

<span data-ttu-id="7df05-126">[Таблица инсталлексекутесекуенце](installexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="7df05-126">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="7df05-127">Действие</span><span class="sxs-lookup"><span data-stu-id="7df05-127">Action</span></span>          | <span data-ttu-id="7df05-128">Условие</span><span class="sxs-lookup"><span data-stu-id="7df05-128">Condition</span></span>  |
|-----------------|------------|
| <span data-ttu-id="7df05-129">Функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="7df05-129">InstallFinalize</span></span> | <span data-ttu-id="7df05-130">MyProperty</span><span class="sxs-lookup"><span data-stu-id="7df05-130">Myproperty</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7df05-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7df05-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7df05-132">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="7df05-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



