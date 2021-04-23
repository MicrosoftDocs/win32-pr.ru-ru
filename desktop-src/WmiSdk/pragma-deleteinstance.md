---
description: Удаляет существующий экземпляр класса из репозитория.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma DeleteInstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080417"
---
# <a name="pragma-deleteinstance"></a><span data-ttu-id="f78b6-103">pragma DeleteInstance</span><span class="sxs-lookup"><span data-stu-id="f78b6-103">pragma deleteinstance</span></span>

<span data-ttu-id="f78b6-104">Команда **pragma DeleteInstance** удаляет существующий экземпляр класса из репозитория.</span><span class="sxs-lookup"><span data-stu-id="f78b6-104">The **pragma deleteinstance** command deletes an existing instance of a class from the repository.</span></span>

<span data-ttu-id="f78b6-105">Ниже описан синтаксис для этой команды:</span><span class="sxs-lookup"><span data-stu-id="f78b6-105">The following describes the syntax for this command:</span></span>


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



<span data-ttu-id="f78b6-106">*InstanceId* — это уникальный идентификатор экземпляра, который удаляется компилятором MOF из текущего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f78b6-106">*InstanceId* is a unique identifier of the instance the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="f78b6-107">*\[ Флаг \]* должен быть одним из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="f78b6-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="f78b6-108">Flag</span><span class="sxs-lookup"><span data-stu-id="f78b6-108">Flag</span></span>   | <span data-ttu-id="f78b6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f78b6-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f78b6-110">fail</span><span class="sxs-lookup"><span data-stu-id="f78b6-110">fail</span></span>   | <span data-ttu-id="f78b6-111">Приводит к выходу компилятора MOF с сообщением об ошибке, если класс еще не существует в репозитории.</span><span class="sxs-lookup"><span data-stu-id="f78b6-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="f78b6-112">nofail</span><span class="sxs-lookup"><span data-stu-id="f78b6-112">nofail</span></span> | <span data-ttu-id="f78b6-113">Приводит к тому, что компилятор MOF продолжит работу, даже если класс еще не существует.</span><span class="sxs-lookup"><span data-stu-id="f78b6-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="f78b6-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="f78b6-114">Examples</span></span>

<span data-ttu-id="f78b6-115">В следующем примере показано, как использовать эту команду.</span><span class="sxs-lookup"><span data-stu-id="f78b6-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a><span data-ttu-id="f78b6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f78b6-116">Requirements</span></span>



| <span data-ttu-id="f78b6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f78b6-117">Requirement</span></span> | <span data-ttu-id="f78b6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f78b6-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f78b6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f78b6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f78b6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f78b6-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f78b6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f78b6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f78b6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f78b6-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f78b6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f78b6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78b6-124">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="f78b6-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




