---
description: ICEM06 проверяет наличие недопустимых прямых ссылок на функции модуля.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910380"
---
# <a name="icem06"></a><span data-ttu-id="b9855-103">ICEM06</span><span class="sxs-lookup"><span data-stu-id="b9855-103">ICEM06</span></span>

<span data-ttu-id="b9855-104">ICEM06 проверяет наличие недопустимых прямых ссылок на функции модуля.</span><span class="sxs-lookup"><span data-stu-id="b9855-104">ICEM06 checks for invalid direct references to features by the module.</span></span>

<span data-ttu-id="b9855-105">Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.</span><span class="sxs-lookup"><span data-stu-id="b9855-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="b9855-106">Результат</span><span class="sxs-lookup"><span data-stu-id="b9855-106">Result</span></span>

<span data-ttu-id="b9855-107">ICEM06 отправляет сообщение об ошибке, если база данных модуля содержит прямые ссылки на компонент.</span><span class="sxs-lookup"><span data-stu-id="b9855-107">ICEM06 posts an error when the module database contains direct references to a feature.</span></span> <span data-ttu-id="b9855-108">Сведения о компоненте должны предоставляться пользователем модуля.</span><span class="sxs-lookup"><span data-stu-id="b9855-108">Feature information must be provided by the user of the module.</span></span>

## <a name="example"></a><span data-ttu-id="b9855-109">Пример</span><span class="sxs-lookup"><span data-stu-id="b9855-109">Example</span></span>

<span data-ttu-id="b9855-110">ICEM06 отправляет следующие сообщения об ошибках для модуля, содержащего записи базы данных, показанные ниже.</span><span class="sxs-lookup"><span data-stu-id="b9855-110">ICEM06 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

<span data-ttu-id="b9855-111">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="b9855-111">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="b9855-112">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="b9855-112">Shortcut</span></span>          | <span data-ttu-id="b9855-113">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="b9855-113">Target</span></span>                                 |
|-------------------|----------------------------------------|
| <span data-ttu-id="b9855-114">Shortcut1. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="b9855-114">Shortcut1.*GUID1*</span></span> | <span data-ttu-id="b9855-115">cmd.exe</span><span class="sxs-lookup"><span data-stu-id="b9855-115">cmd.exe</span></span>                                |
| <span data-ttu-id="b9855-116">Shortcut2. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="b9855-116">Shortcut2.*GUID1*</span></span> | <span data-ttu-id="b9855-117">\[мипроп\]</span><span class="sxs-lookup"><span data-stu-id="b9855-117">\[MyProp\]</span></span>                             |
| <span data-ttu-id="b9855-118">Shortcut3. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="b9855-118">Shortcut3.*GUID1*</span></span> | {00000000-0000-0000-0000-000000000000} |



 

<span data-ttu-id="b9855-119">[Таблица классов](class-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="b9855-119">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="b9855-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="b9855-120">CLSID</span></span>   | <span data-ttu-id="b9855-121">Контекст</span><span class="sxs-lookup"><span data-stu-id="b9855-121">Context</span></span>       | <span data-ttu-id="b9855-122">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="b9855-122">Component\_</span></span> | <span data-ttu-id="b9855-123">Функция\_</span><span class="sxs-lookup"><span data-stu-id="b9855-123">Feature\_</span></span>                              |
|---------|---------------|-------------|----------------------------------------|
| <span data-ttu-id="b9855-124">*GUID1*</span><span class="sxs-lookup"><span data-stu-id="b9855-124">*GUID1*</span></span> | <span data-ttu-id="b9855-125">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b9855-125">LocalServer32</span></span> | <span data-ttu-id="b9855-126">Component1</span><span class="sxs-lookup"><span data-stu-id="b9855-126">Component1</span></span>  | {00000000-0000-0000-0000-000000000000} |
| <span data-ttu-id="b9855-127">*GUID2*</span><span class="sxs-lookup"><span data-stu-id="b9855-127">*GUID2*</span></span> | <span data-ttu-id="b9855-128">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b9855-128">LocalServer32</span></span> | <span data-ttu-id="b9855-129">Component2</span><span class="sxs-lookup"><span data-stu-id="b9855-129">Component2</span></span>  | <span data-ttu-id="b9855-130">мифеатуре</span><span class="sxs-lookup"><span data-stu-id="b9855-130">MyFeature</span></span>                              |



 

<span data-ttu-id="b9855-131">ICEM06 сообщает о первой ошибке, так как первая запись в таблице ярлыков содержит запись в целевом поле, которая не является свойством или идентификатором GUID null.</span><span class="sxs-lookup"><span data-stu-id="b9855-131">ICEM06 reports the first error because the first record in the Shortcut table has an entry in the Target field that is not a property or a null GUID.</span></span> <span data-ttu-id="b9855-132">Модуль не может ссылаться на функцию напрямую.</span><span class="sxs-lookup"><span data-stu-id="b9855-132">A module cannot reference a feature directly.</span></span> <span data-ttu-id="b9855-133">Сведения о компоненте должны предоставляться пользователем модуля.</span><span class="sxs-lookup"><span data-stu-id="b9855-133">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="b9855-134">Чтобы устранить эту ошибку, ссылки на компонент следует заменить на идентификатор GUID null.</span><span class="sxs-lookup"><span data-stu-id="b9855-134">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

<span data-ttu-id="b9855-135">ICEM06 сообщает о второй ошибке, так как вторая запись в таблице классов содержит запись в поле функции, которая не является идентификатором GUID null.</span><span class="sxs-lookup"><span data-stu-id="b9855-135">ICEM06 reports the second error because the second record in the Class table has an entry in the Feature field that is not a null GUID.</span></span> <span data-ttu-id="b9855-136">Модуль не может ссылаться на функцию напрямую.</span><span class="sxs-lookup"><span data-stu-id="b9855-136">A module cannot reference a feature directly.</span></span> <span data-ttu-id="b9855-137">Сведения о компоненте должны предоставляться пользователем модуля.</span><span class="sxs-lookup"><span data-stu-id="b9855-137">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="b9855-138">Чтобы устранить эту ошибку, ссылки на компонент следует заменить на идентификатор GUID null.</span><span class="sxs-lookup"><span data-stu-id="b9855-138">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9855-139">См. также</span><span class="sxs-lookup"><span data-stu-id="b9855-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9855-140">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="b9855-140">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



