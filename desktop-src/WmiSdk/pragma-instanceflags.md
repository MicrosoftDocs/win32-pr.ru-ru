---
description: Управляет способом создания или обновления экземпляров в зависимости от указанных флагов.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma инстанцефлагс
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272578"
---
# <a name="pragma-instanceflags"></a><span data-ttu-id="866bf-103">pragma инстанцефлагс</span><span class="sxs-lookup"><span data-stu-id="866bf-103">pragma instanceflags</span></span>

<span data-ttu-id="866bf-104">Команда препроцессора **pragma инстанцефлагс** определяет способ создания или обновления экземпляров в зависимости от указанных флагов.</span><span class="sxs-lookup"><span data-stu-id="866bf-104">The **pragma instanceflags** preprocessor command controls the way instances are created or updated depending on the flags specified.</span></span>

<span data-ttu-id="866bf-105">Ниже описан синтаксис.</span><span class="sxs-lookup"><span data-stu-id="866bf-105">The following describes the syntax:</span></span>


```mof
#pragma instanceflags ([Flag])
```



<span data-ttu-id="866bf-106">*\[ Флаг \]* должен быть одним из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="866bf-106">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="866bf-107">Flag</span><span class="sxs-lookup"><span data-stu-id="866bf-107">Flag</span></span>       | <span data-ttu-id="866bf-108">Описание</span><span class="sxs-lookup"><span data-stu-id="866bf-108">Description</span></span>                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="866bf-109">креатеонли</span><span class="sxs-lookup"><span data-stu-id="866bf-109">createonly</span></span> | <span data-ttu-id="866bf-110">Предотвращает изменение компилятором существующих экземпляров в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="866bf-110">Prevents the compiler from changing any existing instances in the MOF file.</span></span>                                |
| <span data-ttu-id="866bf-111">упдатеонли</span><span class="sxs-lookup"><span data-stu-id="866bf-111">updateonly</span></span> | <span data-ttu-id="866bf-112">Запрещает компилятору создавать новые экземпляры, если экземпляр, указанный в MOF-файле, не существует.</span><span class="sxs-lookup"><span data-stu-id="866bf-112">Prevents the compiler from creating new instances if an instance specified in the MOF file does not exist.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="866bf-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="866bf-113">Examples</span></span>

<span data-ttu-id="866bf-114">В следующем примере показано, как использовать эту команду.</span><span class="sxs-lookup"><span data-stu-id="866bf-114">The following example shows how to use this command.</span></span>


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a><span data-ttu-id="866bf-115">Требования</span><span class="sxs-lookup"><span data-stu-id="866bf-115">Requirements</span></span>



| <span data-ttu-id="866bf-116">Требование</span><span class="sxs-lookup"><span data-stu-id="866bf-116">Requirement</span></span> | <span data-ttu-id="866bf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="866bf-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="866bf-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="866bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="866bf-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="866bf-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="866bf-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="866bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="866bf-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="866bf-121">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="866bf-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="866bf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866bf-123">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="866bf-123">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




