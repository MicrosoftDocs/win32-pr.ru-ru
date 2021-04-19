---
description: Управляет тем, как инструментарий WMI создает или обновляет классы в зависимости от указанных флагов.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma классфлагс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692576"
---
# <a name="pragma-classflags"></a><span data-ttu-id="10fcf-103">pragma классфлагс</span><span class="sxs-lookup"><span data-stu-id="10fcf-103">pragma classflags</span></span>

<span data-ttu-id="10fcf-104">Команда препроцессора **pragma классфлагс** определяет способ создания или обновления классов WMI в зависимости от указанных флагов.</span><span class="sxs-lookup"><span data-stu-id="10fcf-104">The **pragma classflags** preprocessor command controls the way WMI creates or updates classes depending on the flags specified.</span></span>

<span data-ttu-id="10fcf-105">Ниже описан синтаксис для этой команды:</span><span class="sxs-lookup"><span data-stu-id="10fcf-105">The following describes the syntax for this command:</span></span>


```mof
#pragma classflags ("[flag1], [flag2]")
```



<span data-ttu-id="10fcf-106">*\[ Флаг \]* должен быть одним или несколькими из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="10fcf-106">*\[Flag\]* must be one or more of the following arguments.</span></span> <span data-ttu-id="10fcf-107">Можно сочетать любые флаги, не противоречащие друг другу.</span><span class="sxs-lookup"><span data-stu-id="10fcf-107">You can combine any flags that do not contradict each other.</span></span>



| <span data-ttu-id="10fcf-108">Flag</span><span class="sxs-lookup"><span data-stu-id="10fcf-108">Flag</span></span>        | <span data-ttu-id="10fcf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="10fcf-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10fcf-110">креатеонли</span><span class="sxs-lookup"><span data-stu-id="10fcf-110">createonly</span></span>  | <span data-ttu-id="10fcf-111">Указывает компилятору не вносить изменения в существующие классы и завершает компиляцию, если класс, указанный в MOF-файле, уже существует в WMI.</span><span class="sxs-lookup"><span data-stu-id="10fcf-111">Instructs the compiler not make any changes to existing classes and terminates a compilation if a class specified in the MOF file already exists in WMI.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="10fcf-112">форцеупдате</span><span class="sxs-lookup"><span data-stu-id="10fcf-112">forceupdate</span></span> | <span data-ttu-id="10fcf-113">Принудительно обновляет классы при наличии конфликтующих дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="10fcf-113">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="10fcf-114">Например, если определить квалификатор класса в дочернем классе, и базовый класс попытается добавить тот же квалификатор, использование этого флага приводит к устранению этого конфликта компилятором путем удаления конфликтующего квалификатора в дочернем классе.</span><span class="sxs-lookup"><span data-stu-id="10fcf-114">For example, if you define a class qualifier in a child class and the base class attempts to add the same qualifier, using this flag causes the compiler to resolve this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="10fcf-115">Если дочерний класс имеет экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="10fcf-115">If the child class has instances, the update fails.</span></span> |
| <span data-ttu-id="10fcf-116">сафеупдате</span><span class="sxs-lookup"><span data-stu-id="10fcf-116">safeupdate</span></span>  | <span data-ttu-id="10fcf-117">Позволяет компилятору обновлять классы даже в случае существования дочерних классов, если изменение не вызывает конфликты с дочерними классами.</span><span class="sxs-lookup"><span data-stu-id="10fcf-117">Allows the compiler to update classes even if child classes exist, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="10fcf-118">Например, этот флаг позволяет добавить новое свойство в базовый класс без необходимости добавления свойства в любой существующий дочерний класс.</span><span class="sxs-lookup"><span data-stu-id="10fcf-118">For example, this flag allows you to add a new property to a base class without also having to add the property to any pre-existing child class.</span></span> <span data-ttu-id="10fcf-119">Если дочерние классы имеют экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="10fcf-119">If the child classes have instances, the update fails.</span></span>                           |
| <span data-ttu-id="10fcf-120">упдатеонли</span><span class="sxs-lookup"><span data-stu-id="10fcf-120">updateonly</span></span>  | <span data-ttu-id="10fcf-121">Указывает компилятору не создавать новые классы и приводит к тому, что компилятор завершит компиляцию, если класс, указанный в MOF-файле, не существует.</span><span class="sxs-lookup"><span data-stu-id="10fcf-121">Instructs the compiler to not create any new classes and causes the compiler to terminate the compilation if a class specified in the MOF file does not exist.</span></span>                                                                                                                                                                                                  |



 

## <a name="examples"></a><span data-ttu-id="10fcf-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="10fcf-122">Examples</span></span>

<span data-ttu-id="10fcf-123">В следующем примере показано, как использовать эту команду с флагами упдатеонли и форцеупдате.</span><span class="sxs-lookup"><span data-stu-id="10fcf-123">The following example shows how to use this command with the updateonly and forceupdate flags.</span></span>


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a><span data-ttu-id="10fcf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="10fcf-124">Requirements</span></span>



| <span data-ttu-id="10fcf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="10fcf-125">Requirement</span></span> | <span data-ttu-id="10fcf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="10fcf-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="10fcf-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10fcf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10fcf-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10fcf-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="10fcf-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10fcf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10fcf-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10fcf-130">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10fcf-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10fcf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fcf-132">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="10fcf-132">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




