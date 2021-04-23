---
description: Удаляет существующий класс и его экземпляры из репозитория.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma делетекласс
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913208"
---
# <a name="pragma-deleteclass"></a><span data-ttu-id="45bf6-103">pragma делетекласс</span><span class="sxs-lookup"><span data-stu-id="45bf6-103">pragma deleteclass</span></span>

<span data-ttu-id="45bf6-104">Команда препроцессора **pragma делетекласс** удаляет существующий класс и его экземпляры из репозитория.</span><span class="sxs-lookup"><span data-stu-id="45bf6-104">The **pragma deleteclass** preprocessor command deletes an existing class and its instances from the repository.</span></span>

<span data-ttu-id="45bf6-105">Ниже описан синтаксис.</span><span class="sxs-lookup"><span data-stu-id="45bf6-105">The following describes the syntax:</span></span>


```mof
#pragma deleteclass("ClassName", [Flag])
```



<span data-ttu-id="45bf6-106">*ClassName* — имя класса, который компилятор MOF удаляет из текущего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="45bf6-106">*ClassName* is the name of the class that the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="45bf6-107">*\[ Флаг \]* должен быть одним из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="45bf6-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="45bf6-108">Flag</span><span class="sxs-lookup"><span data-stu-id="45bf6-108">Flag</span></span>   | <span data-ttu-id="45bf6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="45bf6-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bf6-110">fail</span><span class="sxs-lookup"><span data-stu-id="45bf6-110">fail</span></span>   | <span data-ttu-id="45bf6-111">Приводит к выходу компилятора MOF с сообщением об ошибке, если класс еще не существует в репозитории.</span><span class="sxs-lookup"><span data-stu-id="45bf6-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="45bf6-112">nofail</span><span class="sxs-lookup"><span data-stu-id="45bf6-112">nofail</span></span> | <span data-ttu-id="45bf6-113">Приводит к тому, что компилятор MOF продолжит работу, даже если класс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="45bf6-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="45bf6-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="45bf6-114">Examples</span></span>

<span data-ttu-id="45bf6-115">В следующем примере показано, как использовать эту команду.</span><span class="sxs-lookup"><span data-stu-id="45bf6-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a><span data-ttu-id="45bf6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="45bf6-116">Requirements</span></span>



| <span data-ttu-id="45bf6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="45bf6-117">Requirement</span></span> | <span data-ttu-id="45bf6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="45bf6-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="45bf6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45bf6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45bf6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45bf6-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="45bf6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45bf6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45bf6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45bf6-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45bf6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45bf6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45bf6-124">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="45bf6-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




