---
title: RPC_MGR_EPV (Рпкдце. h)
description: Тип данных \_ ЕПВ ДИСПЕТЧЕРА RPC \_ определяет вектор точки входа диспетчера.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801312"
---
# <a name="rpc_mgr_epv"></a><span data-ttu-id="aafe0-104">\_ЕПВ ДИСПЕТЧЕРА \_ RPC</span><span class="sxs-lookup"><span data-stu-id="aafe0-104">RPC\_MGR\_EPV</span></span>

<span data-ttu-id="aafe0-105">Тип данных **\_ \_ ЕПВ диспетчера RPC** определяет вектор точки входа диспетчера.</span><span class="sxs-lookup"><span data-stu-id="aafe0-105">The data type **RPC\_MGR\_EPV** defines a manager entry-point vector.</span></span>

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a><span data-ttu-id="aafe0-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="aafe0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aafe0-107"><span id="if-name"></span><span id="IF-NAME"></span>**If-Name**</span><span class="sxs-lookup"><span data-stu-id="aafe0-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span></span>
</dt> <dd>

<span data-ttu-id="aafe0-108">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aafe0-108">Specifies the name of the interface</span></span>

</dd> <dt>

<span data-ttu-id="aafe0-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**Тип возвращаемого значения**</span><span class="sxs-lookup"><span data-stu-id="aafe0-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**</span></span>
</dt> <dd>

<span data-ttu-id="aafe0-110">Указывает тип, возвращаемый функцией **FunctionName** , указанной в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="aafe0-110">Specifies the type returned by the function **Functionname** indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="aafe0-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**</span><span class="sxs-lookup"><span data-stu-id="aafe0-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span></span>
</dt> <dd>

<span data-ttu-id="aafe0-112">Указывает имя функции, указанной в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="aafe0-112">Specifies the name of the function indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="aafe0-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**Param-List**</span><span class="sxs-lookup"><span data-stu-id="aafe0-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span></span>
</dt> <dd>

<span data-ttu-id="aafe0-114">Задает параметры, указанные для функции **FunctionName** в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="aafe0-114">Specifies the parameters indicated for the function **Functionname** in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aafe0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aafe0-115">Remarks</span></span>

<span data-ttu-id="aafe0-116">Вектор точки входа диспетчера (ЕПВ) является массивом указателей на функции.</span><span class="sxs-lookup"><span data-stu-id="aafe0-116">The manager entry-point vector (EPV) is an array of function pointers.</span></span> <span data-ttu-id="aafe0-117">Массив содержит указатели на реализации функций, указанных в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="aafe0-117">The array contains pointers to the implementations of the functions specified in the IDL file.</span></span> <span data-ttu-id="aafe0-118">Число элементов в массиве равно числу функций, указанных в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="aafe0-118">The number of elements in the array is set to the number of functions specified in the IDL file.</span></span> <span data-ttu-id="aafe0-119">Приложение может также иметь несколько Епвс, представляющих несколько реализаций функций, указанных в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="aafe0-119">An application can also have multiple EPVs, representing multiple implementations of the functions specified in the interface.</span></span>

<span data-ttu-id="aafe0-120">Компилятор MIDL создает тип данных **ЕПВ** по умолчанию, именуемый \* if-Name \***\_ Server \_ ЕПВ**, где *If-Name* указывает идентификатор интерфейса в файле IDL.</span><span class="sxs-lookup"><span data-stu-id="aafe0-120">The MIDL compiler generates a default **EPV** data type named \*if-name\***\_SERVER\_EPV**, where *if-name* specifies the interface identifier in the IDL file.</span></span> <span data-ttu-id="aafe0-121">Компилятор MIDL Инициализирует этот **ЕПВ** по умолчанию, чтобы он содержал указатели на функции для каждой процедуры, указанной в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="aafe0-121">The MIDL compiler initializes this default **EPV** to contain function pointers for each of the procedures specified in the IDL file.</span></span>

<span data-ttu-id="aafe0-122">Если сервер предлагает несколько реализаций одного интерфейса, серверное приложение должно объявлять и инициализировать одну переменную типа *If-Name \* \* \* \_ Server \_ ЕПВ*\* для каждой реализации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aafe0-122">When the server offers multiple implementations of the same interface, the server application must declare and initialize one variable of type *if-name\*\*\*\_SERVER\_EPV*\* for each implementation of the interface.</span></span> <span data-ttu-id="aafe0-123">Каждый **ЕПВ** должен содержать одну точку входа (указатель на функцию) для каждой процедуры, определенной в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="aafe0-123">Each **EPV** must contain one entry point (function pointer) for each procedure defined in the IDL file.</span></span>

## <a name="requirements"></a><span data-ttu-id="aafe0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="aafe0-124">Requirements</span></span>



| <span data-ttu-id="aafe0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="aafe0-125">Requirement</span></span> | <span data-ttu-id="aafe0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="aafe0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aafe0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aafe0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="aafe0-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aafe0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aafe0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aafe0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="aafe0-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aafe0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aafe0-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aafe0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="aafe0-132"><dt>Рпкдце. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aafe0-132"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aafe0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aafe0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aafe0-134">**рпксерверрегистериф**</span><span class="sxs-lookup"><span data-stu-id="aafe0-134">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[<span data-ttu-id="aafe0-135">**RpcServerRegisterIf2**</span><span class="sxs-lookup"><span data-stu-id="aafe0-135">**RpcServerRegisterIf2**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[<span data-ttu-id="aafe0-136">**рпксерверрегистерифекс**</span><span class="sxs-lookup"><span data-stu-id="aafe0-136">**RpcServerRegisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[<span data-ttu-id="aafe0-137">**рпксерверунрегистериф**</span><span class="sxs-lookup"><span data-stu-id="aafe0-137">**RpcServerUnregisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[<span data-ttu-id="aafe0-138">**рпксерверунрегистерифекс**</span><span class="sxs-lookup"><span data-stu-id="aafe0-138">**RpcServerUnregisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





