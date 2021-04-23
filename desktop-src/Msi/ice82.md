---
description: ICE82 проверяет, что действие Регистерпродукт, действие RegisterUser, действие Публишпродукт и действие Публишфеатурес представлены в таблице Инсталлексекутесекуенце. Пакет проверяется, если имеются все действия.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816241"
---
# <a name="ice82"></a><span data-ttu-id="f0ad4-104">ICE82</span><span class="sxs-lookup"><span data-stu-id="f0ad4-104">ICE82</span></span>

<span data-ttu-id="f0ad4-105">ICE82 проверяет, что действие [регистерпродукт](registerproduct-action.md), действие [RegisterUser](registeruser-action.md), [действие публишпродукт](publishproduct-action.md)и [действие публишфеатурес](publishfeatures-action.md) представлены в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0ad4-105">ICE82 validates that the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) are all present in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="f0ad4-106">Пакет проверяется, если имеются все действия.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-106">The package is validated if all the actions are present.</span></span>

<span data-ttu-id="f0ad4-107">ICE82 отправляет предупреждение при наличии двух действий с одним порядковым номером, указанным в таблицах Инсталлексекутесекуенце, Инсталлуисекуенце, Админексекутесекуенце, Админуисекуенце или Адвтексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-107">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables .</span></span>

## <a name="result"></a><span data-ttu-id="f0ad4-108">Результат</span><span class="sxs-lookup"><span data-stu-id="f0ad4-108">Result</span></span>

<span data-ttu-id="f0ad4-109">ICE82 отправляет следующие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-109">ICE82 posts the following warnings.</span></span>



| <span data-ttu-id="f0ad4-110">Предупреждение ICE82</span><span class="sxs-lookup"><span data-stu-id="f0ad4-110">ICE82 warning</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="f0ad4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f0ad4-111">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ad4-112">Таблица Инсталлексекутесекуенце не содержит набор действий, упомянутых ниже: отсутствуют действия:</span><span class="sxs-lookup"><span data-stu-id="f0ad4-112">The InstallExecuteSequence table does not contain the set of actions mentioned below: Actions Missing:</span></span><br/> <span data-ttu-id="f0ad4-113">Публикация компонентов</span><span class="sxs-lookup"><span data-stu-id="f0ad4-113">Publish Features</span></span><br/> <span data-ttu-id="f0ad4-114">Публикация продукта</span><span class="sxs-lookup"><span data-stu-id="f0ad4-114">Publish Product</span></span><br/> <span data-ttu-id="f0ad4-115">Регистрация продукта</span><span class="sxs-lookup"><span data-stu-id="f0ad4-115">Register Product</span></span><br/> <span data-ttu-id="f0ad4-116">Регистрация пользователя</span><span class="sxs-lookup"><span data-stu-id="f0ad4-116">Register User</span></span><br/> | <span data-ttu-id="f0ad4-117">Настраиваемое действие ICE82 отправляет предупреждение, если все четыре действия отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-117">ICE82 custom action posts a warning if all four actions are absent.</span></span>                                                                                                                                         |
| <span data-ttu-id="f0ad4-118">Это действие \[ 1 \] содержит копию порядкового номера \[ 2 \] в таблице \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="f0ad4-118">This action \[1\] has duplicate sequence number \[2\] in the table \[3\].</span></span>                                                                                                                                                     | <span data-ttu-id="f0ad4-119">ICE82 отправляет предупреждение при наличии двух действий с одним порядковым номером, указанным в таблицах Инсталлексекутесекуенце, Инсталлуисекуенце, Админексекутесекуенце, Админуисекуенце или Адвтексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-119">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables.</span></span> |



 

<span data-ttu-id="f0ad4-120">ICE82 отправляет следующие ошибки.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-120">ICE82 posts the following errors.</span></span>



| <span data-ttu-id="f0ad4-121">ICE82, ошибка</span><span class="sxs-lookup"><span data-stu-id="f0ad4-121">ICE82 error</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="f0ad4-122">Описание</span><span class="sxs-lookup"><span data-stu-id="f0ad4-122">Description</span></span>                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ad4-123">Инсталлексекутесекуенце должен содержать все действия, упомянутые ниже, или ни одно из них не представим ни одного действия.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-123">The InstallExecuteSequence should either contain all of the actions mentioned below or none of them Actions Present</span></span><br/> <List of actions present> <br/> <span data-ttu-id="f0ad4-124">Отсутствуют действия:</span><span class="sxs-lookup"><span data-stu-id="f0ad4-124">Actions Missing:</span></span><br/> <List of actions missing> <br/> | <span data-ttu-id="f0ad4-125">ICE82 отправляет сообщение об ошибке, если имеются некоторые из четырех действий, а другие отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="f0ad4-125">ICE82 posts an error if some of the four actions are present and others are absent.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f0ad4-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f0ad4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0ad4-127">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="f0ad4-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




