---
title: RPC_IF_HANDLE (Рпкдце. h)
description: '\_ \_ Тип данных RPC if Handle объявляет обработчик интерфейса.'
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989119"
---
# <a name="rpc_if_handle"></a><span data-ttu-id="4cdc9-104">RPC \_ if \_ Handle</span><span class="sxs-lookup"><span data-stu-id="4cdc9-104">RPC\_IF\_HANDLE</span></span>

<span data-ttu-id="4cdc9-105">Тип данных **RPC \_ if \_ Handle** объявляет обработчик интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-105">The **RPC\_IF\_HANDLE** data type declares an interface handle.</span></span>


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="4cdc9-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cdc9-106">Remarks</span></span>

<span data-ttu-id="4cdc9-107">Библиотека времени выполнения RPC использует дескрипторы интерфейса для доступа к структуре данных спецификации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-107">The RPC run-time library uses interface handles to access the interface-specification data structure.</span></span> <span data-ttu-id="4cdc9-108">Компилятор MIDL автоматически создает структуру данных спецификации интерфейса из каждого IDL-файла и создает глобальную переменную типа RPC, \_ Если \_ Handle для спецификации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-108">The MIDL compiler automatically creates an interface-specification data structure from each IDL file and creates a global variable of type RPC\_IF\_HANDLE for the interface specification.</span></span>

<span data-ttu-id="4cdc9-109">Компилятор MIDL включает в каждый файл заголовка, созданный для интерфейса, обработчик интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-109">The MIDL compiler includes an interface handle in each header file generated for the interface.</span></span> <span data-ttu-id="4cdc9-110">Функции, для которых в качестве параметра указан интерфейс, отображают тип данных **RPC \_ при \_ обработке**.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-110">Functions requiring the interface specification as a parameter show a data type of **RPC\_IF\_HANDLE**.</span></span> <span data-ttu-id="4cdc9-111">Имя каждого обработчика интерфейса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4cdc9-111">The form of each interface handle name is as follows:</span></span>

-   <span data-ttu-id="4cdc9-112">*If-Name* \_ Клиентифхандле (для клиента)</span><span class="sxs-lookup"><span data-stu-id="4cdc9-112">*if-name*\_ClientIfHandle (for the client)</span></span>
-   <span data-ttu-id="4cdc9-113">*If-Name* \_ Серверифхандле (для сервера)</span><span class="sxs-lookup"><span data-stu-id="4cdc9-113">*if-name*\_ServerIfHandle (for the server)</span></span>

<span data-ttu-id="4cdc9-114">В части *If-Name* указывается идентификатор интерфейса в файле IDL.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-114">The *if-name* part specifies the interface identifier in the IDL file.</span></span>

<span data-ttu-id="4cdc9-115">Пример:</span><span class="sxs-lookup"><span data-stu-id="4cdc9-115">For example:</span></span>

<span data-ttu-id="4cdc9-116">Привет, \_ клиентифхандле</span><span class="sxs-lookup"><span data-stu-id="4cdc9-116">hello\_ClientIfHandle</span></span>

<span data-ttu-id="4cdc9-117">Привет, \_ серверифхандле</span><span class="sxs-lookup"><span data-stu-id="4cdc9-117">hello\_ServerIfHandle</span></span>

> [!Note]  
> <span data-ttu-id="4cdc9-118">Максимальная длина имени маркера интерфейса — 31 символ.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-118">The maximum length of the interface handle name is 31 characters.</span></span>

 

<span data-ttu-id="4cdc9-119">Так как \_ части имен "клиентифхандле" и " \_ серверифхандле" должны содержать 15 символов, Длина элемента *If-Name* не может превышать 16 символов.</span><span class="sxs-lookup"><span data-stu-id="4cdc9-119">Because the "\_ClientIfHandle" and "\_ServerIfHandle" parts of the names require 15 characters, the *if-name* element can be no more than 16 characters long.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cdc9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4cdc9-120">Requirements</span></span>



| <span data-ttu-id="4cdc9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4cdc9-121">Requirement</span></span> | <span data-ttu-id="4cdc9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4cdc9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdc9-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cdc9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4cdc9-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cdc9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4cdc9-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cdc9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4cdc9-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cdc9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4cdc9-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4cdc9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cdc9-128"><dt>Рпкдце. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cdc9-128"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





