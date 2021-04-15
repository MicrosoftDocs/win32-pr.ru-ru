---
description: Если не удается найти необходимые средства оценки согласованности для существующих настраиваемых действий ICE, перечисленных в справочнике по ICE, необходимо подготовить собственный ICE для проверки пакета.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Сборка ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662916"
---
# <a name="building-an-ice"></a><span data-ttu-id="9766e-103">Сборка ICE</span><span class="sxs-lookup"><span data-stu-id="9766e-103">Building An ICE</span></span>

<span data-ttu-id="9766e-104">Если не удается найти необходимые средства [оценки согласованности](internal-consistency-evaluators-ices.md) для существующих настраиваемых действий Ice, перечисленных в [справочнике по Ice](ice-reference.md), необходимо подготовить собственный ICE для проверки пакета.</span><span class="sxs-lookup"><span data-stu-id="9766e-104">If you are unable to find the [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) you need among the existing ICE custom actions listed in the [ICE Reference](ice-reference.md), you will need to prepare your own ICE to validate your package.</span></span>

<span data-ttu-id="9766e-105">При создании настраиваемых действий ICE необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9766e-105">When authoring ICE custom actions you should do the following:</span></span>

-   <span data-ttu-id="9766e-106">Значение ICEs основано только на пользовательских действиях типов, перечисленных в приведенной таблице.</span><span class="sxs-lookup"><span data-stu-id="9766e-106">Base the ICEs only on custom actions of types listed in the table shown.</span></span>
-   <span data-ttu-id="9766e-107">Вызовите [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) и опубликуйте \_ Пользовательский тип сообщения инсталлмессаже.</span><span class="sxs-lookup"><span data-stu-id="9766e-107">Call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and post an INSTALLMESSAGE\_USER type of message.</span></span> <span data-ttu-id="9766e-108">При создании сообщений ICE следуйте формату сообщения в [рекомендациях по сообщениям компилятора](ice-message-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="9766e-108">When authoring your ICE messages follow the message format in the [ICE Message Guidelines](ice-message-guidelines.md).</span></span>
-   <span data-ttu-id="9766e-109">Напишите свой ICE так, чтобы он записывал все ошибки API и всегда возвращал ошибку \_ успешно.</span><span class="sxs-lookup"><span data-stu-id="9766e-109">Write your ICE such that it captures any API errors and always returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="9766e-110">Это необходимо, чтобы обеспечить выполнение последующих настраиваемых действий после сбоя ICE.</span><span class="sxs-lookup"><span data-stu-id="9766e-110">This is necessary to allow subsequent custom actions to run following the failure of an ICE.</span></span>

<span data-ttu-id="9766e-111">Пользовательские действия ICE ограничены следующими типами настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="9766e-111">ICE custom actions are limited to the following custom action types.</span></span>



| <span data-ttu-id="9766e-112">Тип настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="9766e-112">Custom action type</span></span>                                 | <span data-ttu-id="9766e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9766e-113">Description</span></span>               |
|----------------------------------------------------|---------------------------|
| [<span data-ttu-id="9766e-114">Тип настраиваемого действия 1</span><span class="sxs-lookup"><span data-stu-id="9766e-114">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="9766e-115">Библиотека DLL в двоичном потоке</span><span class="sxs-lookup"><span data-stu-id="9766e-115">DLL in binary stream</span></span>      |
| [<span data-ttu-id="9766e-116">Тип настраиваемого действия 2</span><span class="sxs-lookup"><span data-stu-id="9766e-116">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="9766e-117">EXE в двоичном потоке</span><span class="sxs-lookup"><span data-stu-id="9766e-117">EXE in binary stream</span></span>      |
| [<span data-ttu-id="9766e-118">Тип настраиваемого действия 5</span><span class="sxs-lookup"><span data-stu-id="9766e-118">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="9766e-119">JScript в двоичном потоке</span><span class="sxs-lookup"><span data-stu-id="9766e-119">JScript in binary stream</span></span>  |
| [<span data-ttu-id="9766e-120">Тип настраиваемого действия 6</span><span class="sxs-lookup"><span data-stu-id="9766e-120">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="9766e-121">VBScript в двоичном потоке</span><span class="sxs-lookup"><span data-stu-id="9766e-121">VBScript in binary stream</span></span> |
| [<span data-ttu-id="9766e-122">Тип настраиваемого действия 37</span><span class="sxs-lookup"><span data-stu-id="9766e-122">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="9766e-123">Код JScript в виде строки</span><span class="sxs-lookup"><span data-stu-id="9766e-123">JScript code as string</span></span>    |
| [<span data-ttu-id="9766e-124">Тип настраиваемого действия 38</span><span class="sxs-lookup"><span data-stu-id="9766e-124">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="9766e-125">Код VBScript в виде строки</span><span class="sxs-lookup"><span data-stu-id="9766e-125">VBScript code as string</span></span>   |



 

<span data-ttu-id="9766e-126">При создании настраиваемого действия ICE не следует выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9766e-126">When authoring an ICE custom action, do not do the following:</span></span>

-   <span data-ttu-id="9766e-127">Не следует считать, что обработчик модуля, получающий ICE, является экземпляром установки базы данных установщика.</span><span class="sxs-lookup"><span data-stu-id="9766e-127">Do not assume that the handle to the engine that the ICE receives is an installation instance of the installer database.</span></span> <span data-ttu-id="9766e-128">Если он не является экземпляром установки, некоторые свойства не определяются, исходный и целевой каталоги не разрешаются, а текущие состояния компонентов не определяются.</span><span class="sxs-lookup"><span data-stu-id="9766e-128">If it is not a installation instance, certain properties are not defined, the source and target directories are not resolved, and current feature states are not defined.</span></span>
-   <span data-ttu-id="9766e-129">Не полагайтесь на выполнение какого-либо действия установщика, пользовательского действия или другого ICE.</span><span class="sxs-lookup"><span data-stu-id="9766e-129">Do not rely on the prior execution, or non-execution, of any installer action, custom action, or another ICE.</span></span> <span data-ttu-id="9766e-130">Поскольку в предыдущем модуле ICE могли быть созданы временные столбцы в любой таблице, авторы должны ссылаться на столбцы по имени, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="9766e-130">Because a prior ICE may have created temporary columns in any table, authors should reference columns by name whenever possible.</span></span> <span data-ttu-id="9766e-131">ICEs должен очистить все временные столбцы или таблицы до завершения работы.</span><span class="sxs-lookup"><span data-stu-id="9766e-131">ICEs should cleanup any temporary columns or tables before they exit.</span></span>
-   <span data-ttu-id="9766e-132">Не считайте, что авторы имеют доступ к образу исходного каталога базы данных.</span><span class="sxs-lookup"><span data-stu-id="9766e-132">Do not assume that authors have access to an image of the source directory of the database.</span></span>
-   <span data-ttu-id="9766e-133">Не следует рассчитывать, что изменения, вносимые в базу данных, не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="9766e-133">Do not assume that changes made to the database do not persist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9766e-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9766e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9766e-135">Пример ICE в C++</span><span class="sxs-lookup"><span data-stu-id="9766e-135">Sample ICE in C++</span></span>](sample-ice-in-c-.md)
</dt> <dt>

[<span data-ttu-id="9766e-136">Пример ICE в VBScript</span><span class="sxs-lookup"><span data-stu-id="9766e-136">Sample ICE in VBScript</span></span>](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



