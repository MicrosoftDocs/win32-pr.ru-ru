---
description: ICE90 отправляет предупреждение, если обнаруживает, что каталог ярлыка указан как общедоступное свойство.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908843"
---
# <a name="ice90"></a><span data-ttu-id="7873f-103">ICE90</span><span class="sxs-lookup"><span data-stu-id="7873f-103">ICE90</span></span>

<span data-ttu-id="7873f-104">ICE90 отправляет предупреждение, если обнаруживает, что каталог ярлыка указан как общедоступное свойство.</span><span class="sxs-lookup"><span data-stu-id="7873f-104">ICE90 posts a warning if it finds that a shortcut's directory has been specified as a public property.</span></span> <span data-ttu-id="7873f-105">Имена [общих свойств](public-properties.md) записываются прописными буквами.</span><span class="sxs-lookup"><span data-stu-id="7873f-105">The names of [Public Properties](public-properties.md) are written in uppercase letters.</span></span> <span data-ttu-id="7873f-106">Ярлык, заданный общедоступным свойством, может не работать при изменении значения свойства [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="7873f-106">A shortcut specified by a public property may not work if the value of the [**ALLUSERS**](allusers.md) property changes.</span></span>

<span data-ttu-id="7873f-107">Это настраиваемое действие ICE проверяет таблицу ярлыков и использует таблицу Directory.</span><span class="sxs-lookup"><span data-stu-id="7873f-107">This ICE custom action validates the Shortcut table and uses the Directory table.</span></span> <span data-ttu-id="7873f-108">Если таблица каталогов отсутствует, она возвращается без проверки ярлыка таблицы и не отправляет сообщения об ошибках и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="7873f-108">If the Directory table is not present, it returns without validating the Shortcut table and posts no errors or warnings.</span></span>

## <a name="result"></a><span data-ttu-id="7873f-109">Результат</span><span class="sxs-lookup"><span data-stu-id="7873f-109">Result</span></span>

<span data-ttu-id="7873f-110">ICE90 отправляет следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="7873f-110">ICE90 posts the following warning.</span></span>



| <span data-ttu-id="7873f-111">ICE90, ошибка</span><span class="sxs-lookup"><span data-stu-id="7873f-111">ICE90 error</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="7873f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7873f-112">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="7873f-113">Ярлык " \[ 1 \] " содержит каталог, который является общедоступным свойством (все прописные) и находится в каталоге профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="7873f-113">The shortcut '\[1\]' has a directory that is a public property (ALL CAPS) and is under user profile directory.</span></span> <span data-ttu-id="7873f-114">Это приводит к проблеме, если значение свойства [**ALLUSERS**](allusers.md) изменяется в последовательности пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7873f-114">This results in a problem if the value of the [**ALLUSERS**](allusers.md) property changes in the UI sequence.</span></span> | <span data-ttu-id="7873f-115">Каталог ярлыка был указан как общедоступное свойство.</span><span class="sxs-lookup"><span data-stu-id="7873f-115">A shortcut's directory has been specified as a public property.</span></span> |



 

## <a name="example"></a><span data-ttu-id="7873f-116">Пример</span><span class="sxs-lookup"><span data-stu-id="7873f-116">Example</span></span>

<span data-ttu-id="7873f-117">ICE90 сообщает следующее предупреждение для примера:</span><span class="sxs-lookup"><span data-stu-id="7873f-117">ICE90 reports the following warning for the example:</span></span>

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

<span data-ttu-id="7873f-118">В этом примере MYDIR находится под профилем пользователя.</span><span class="sxs-lookup"><span data-stu-id="7873f-118">In this example, MYDIR is under a users profile.</span></span> <span data-ttu-id="7873f-119">ICE90 отправляет предупреждение, так как расположение целевого каталога указывается общедоступным свойством MYDIR.</span><span class="sxs-lookup"><span data-stu-id="7873f-119">ICE90 posts a warning because the location of the target directory is specified by a public property, MYDIR.</span></span> <span data-ttu-id="7873f-120">Пользователь может изменить свойство MYDIR или [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="7873f-120">A user may change MYDIR or [**ALLUSERS**](allusers.md) property.</span></span> <span data-ttu-id="7873f-121">Если для [контекста установки](installation-context.md)для каждого компьютера задана **ALLUSERS** , а MyDir находится под профилем пользователя, то файл ярлыка в MyDir копируется в профиль "все пользователи", а не в профиль конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7873f-121">If **ALLUSERS** is set for the per-machine [installation context](installation-context.md), and MYDIR is under a users profile, the shortcut file in MYDIR are copied under the "All Users" profile and not a particular user's profile.</span></span> <span data-ttu-id="7873f-122">Если для контекста установки на пользователя задана **ALLUSERS** , файл ярлыка в MyDir копируется в профиль конкретного пользователя и недоступен для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="7873f-122">If **ALLUSERS** is set for the per-user installation context, the shortcut file in MYDIR is copied into a particular user's profile and is not available to other users.</span></span>

<span data-ttu-id="7873f-123">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="7873f-123">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="7873f-124">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="7873f-124">Shortcut</span></span>  | <span data-ttu-id="7873f-125">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="7873f-125">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="7873f-126">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="7873f-126">Shortcut1</span></span> | <span data-ttu-id="7873f-127">MYDIR</span><span class="sxs-lookup"><span data-stu-id="7873f-127">MYDIR</span></span>       |



 

<span data-ttu-id="7873f-128">[Таблица каталогов](directory-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="7873f-128">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="7873f-129">Каталог</span><span class="sxs-lookup"><span data-stu-id="7873f-129">Directory</span></span> | <span data-ttu-id="7873f-130">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="7873f-130">Directory\_Parent</span></span> |
|-----------|-------------------|
| <span data-ttu-id="7873f-131">MYDIR</span><span class="sxs-lookup"><span data-stu-id="7873f-131">MYDIR</span></span>     | <span data-ttu-id="7873f-132">программенуфолдер</span><span class="sxs-lookup"><span data-stu-id="7873f-132">ProgramMenuFolder</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7873f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="7873f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7873f-134">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="7873f-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



