---
description: Функции, перечисленные в следующей таблице, являются точками входа для библиотек DLL средства синтаксического анализа. Функции являются точками входа для вызовов из операционной системы и сетевой монитор.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Функции экспорта библиотеки DLL средства синтаксического анализа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423674"
---
# <a name="parser-dll-export-functions"></a><span data-ttu-id="d93ec-104">Функции экспорта библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="d93ec-104">Parser DLL Export Functions</span></span>

<span data-ttu-id="d93ec-105">Функции, перечисленные в следующей таблице, являются точками входа для библиотек DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="d93ec-105">The functions, listed in the following table, are entry points for parser DLLs.</span></span> <span data-ttu-id="d93ec-106">Функции являются точками входа для вызовов из операционной системы и сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="d93ec-106">The functions are the entry points for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="d93ec-107">Функция</span><span class="sxs-lookup"><span data-stu-id="d93ec-107">Function</span></span>                                           | <span data-ttu-id="d93ec-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d93ec-108">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d93ec-109">Средство синтаксического анализа DllMain</span><span class="sxs-lookup"><span data-stu-id="d93ec-109">DllMain Parser</span></span>](dllmain-parser.md)               | <span data-ttu-id="d93ec-110">Указывает на библиотеку DLL анализатора, которую он загружает или выгружает.</span><span class="sxs-lookup"><span data-stu-id="d93ec-110">Indicates to the parser DLL that it is loaded or unloaded.</span></span> <span data-ttu-id="d93ec-111">Операционная система вызывает функцию **средства синтаксического анализа DllMain** , когда процесс загружает или ВЫГРУЖАЕТ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="d93ec-111">The operating system calls the **DllMain Parser** function when a process loads or unloads the DLL.</span></span> |
| [<span data-ttu-id="d93ec-112">аттачпропертиес</span><span class="sxs-lookup"><span data-stu-id="d93ec-112">AttachProperties</span></span>](attachproperties.md)           | <span data-ttu-id="d93ec-113">Уведомляет средство синтаксического анализа о необходимости присоединения всех свойств, которые существуют в кадре.</span><span class="sxs-lookup"><span data-stu-id="d93ec-113">Notifies the parser to attach any properties that exist in a frame.</span></span>                                                                                            |
| [<span data-ttu-id="d93ec-114">Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="d93ec-114">Deregister</span></span>](deregister.md)                       | <span data-ttu-id="d93ec-115">Уведомляет средство синтаксического анализа о необходимости очистки.</span><span class="sxs-lookup"><span data-stu-id="d93ec-115">Notifies the parser to clean up.</span></span>                                                                                                                               |
| [<span data-ttu-id="d93ec-116">форматпропертиес</span><span class="sxs-lookup"><span data-stu-id="d93ec-116">FormatProperties</span></span>](formatproperties.md)           | <span data-ttu-id="d93ec-117">Уведомляет средство синтаксического анализа, чтобы перевести все экземпляры свойств в и создать элемент **сзпропертитекст** каждой структуры **пропертинст** .</span><span class="sxs-lookup"><span data-stu-id="d93ec-117">Notifies the parser to take all of the property instances in and build the **szPropertyText** member of each **PROPERTYINST** structure.</span></span>                       |
| [<span data-ttu-id="d93ec-118">рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="d93ec-118">RecognizeFrame</span></span>](recognizeframe.md)               | <span data-ttu-id="d93ec-119">Определяет, может ли синтаксический анализатор интерпретировать необработанные данные кадра с указанным Протоколом.</span><span class="sxs-lookup"><span data-stu-id="d93ec-119">Determines whether the parser can interpret the unprocessed frame data with the specified protocol.</span></span>                                                            |
| [<span data-ttu-id="d93ec-120">Регистрация средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="d93ec-120">Register Parser</span></span>](register-parser.md)             | <span data-ttu-id="d93ec-121">Определяет основные сведения о средстве синтаксического анализа в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="d93ec-121">Determines basic information about the parser within the DLL.</span></span> <span data-ttu-id="d93ec-122">Сетевой монитор вызывает функцию **средства синтаксического анализа Register** .</span><span class="sxs-lookup"><span data-stu-id="d93ec-122">Network Monitor calls the **Register Parser** function.</span></span>                                          |
| [<span data-ttu-id="d93ec-123">парсераутоинсталлинфо</span><span class="sxs-lookup"><span data-stu-id="d93ec-123">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md) | <span data-ttu-id="d93ec-124">Автоматически устанавливает средство синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="d93ec-124">Installs a parser automatically.</span></span>                                                                                                                               |



 

<span data-ttu-id="d93ec-125">Сетевой монитор предоставляет структуры и вспомогательные функции, которые может вызывать средство синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="d93ec-125">Network Monitor provides structures and helper functions that the parser can call.</span></span>



| <span data-ttu-id="d93ec-126">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d93ec-126">For more information about</span></span>                          | <span data-ttu-id="d93ec-127">См.</span><span class="sxs-lookup"><span data-stu-id="d93ec-127">See</span></span>                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d93ec-128">Вспомогательные функции, которые могут вызываться экспертами и анализаторами.</span><span class="sxs-lookup"><span data-stu-id="d93ec-128">Helper functions that experts and parsers can call.</span></span> | [<span data-ttu-id="d93ec-129">Общие функции эксперта и средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="d93ec-129">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="d93ec-130">Вспомогательные функции, которые могут вызываться только анализаторами.</span><span class="sxs-lookup"><span data-stu-id="d93ec-130">Helper functions that only parsers can call.</span></span>        | [<span data-ttu-id="d93ec-131">Функции средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="d93ec-131">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="d93ec-132">Структуры, используемые функциями синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="d93ec-132">Structures that parser functions use.</span></span>               | [<span data-ttu-id="d93ec-133">Структуры синтаксического анализатора</span><span class="sxs-lookup"><span data-stu-id="d93ec-133">Parser Structures</span></span>](parser-structures.md)                                   |



 

 

 



