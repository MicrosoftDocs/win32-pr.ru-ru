---
UID: NF:directml.IDMLDevice1.CompileGraph
title: 'IDMLDevice1:: Компилеграф'
description: Компилирует граф операторов Директмл в объект, который можно отправить в GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719908"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="5816c-103">Метод IDMLDevice1:: Компилеграф (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="5816c-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="5816c-104">Компилирует граф операторов Директмл в объект, который можно отправить в GPU.</span><span class="sxs-lookup"><span data-stu-id="5816c-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="5816c-105">Скомпилированный оператор представляет собой эффективную, помогут форму оператора, который подходит для выполнения на GPU.</span><span class="sxs-lookup"><span data-stu-id="5816c-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="5816c-106">Скомпилированный оператор содержит состояние (например, шейдеры и другие объекты), необходимые для выполнения.</span><span class="sxs-lookup"><span data-stu-id="5816c-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="5816c-107">Поскольку скомпилированный оператор реализует интерфейс [идмлпажеабле](/windows/win32/api/directml/nn-directml-idmlpageable) , вы можете при необходимости исключить его из памяти GPU.</span><span class="sxs-lookup"><span data-stu-id="5816c-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="5816c-108">Дополнительные сведения см. в разделе [IDMLDevice1:: вытеснение](/windows/win32/api/directml/nf-directml-idmldevice-evict) и [IDMLDevice1:: макересидент](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .</span><span class="sxs-lookup"><span data-stu-id="5816c-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="5816c-109">Скомпилированный оператор не использует объекты [идмлоператор](/windows/win32/api/directml/nn-directml-idmloperator) , предоставленные в описании графа, и не ссылается на них после того, как этот метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5816c-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5816c-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="5816c-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="5816c-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5816c-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5816c-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5816c-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="5816c-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="5816c-113">Parameters</span></span>

`desc`

<span data-ttu-id="5816c-114">Тип: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5816c-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="5816c-115">Описание графа для компиляции.</span><span class="sxs-lookup"><span data-stu-id="5816c-115">A description of the graph to compile.</span></span> <span data-ttu-id="5816c-116">См. [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="5816c-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="5816c-117">Тип: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="5816c-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="5816c-118">Любые флаги для управления выполнением этого оператора.</span><span class="sxs-lookup"><span data-stu-id="5816c-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="5816c-119">Тип: <b>рефиид</b></span><span class="sxs-lookup"><span data-stu-id="5816c-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="5816c-120">Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в <i>ППВ</i>.</span><span class="sxs-lookup"><span data-stu-id="5816c-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="5816c-121">Это должен быть идентификатор GUID [идмлкомпиледоператор](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span><span class="sxs-lookup"><span data-stu-id="5816c-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="5816c-122">Тип: <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="5816c-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="5816c-123">Указатель на блок памяти, который получает указатель на скомпилированный оператор.</span><span class="sxs-lookup"><span data-stu-id="5816c-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="5816c-124">Это адрес указателя на [идмлкомпиледоператор](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), представляющий созданный скомпилированный оператор.</span><span class="sxs-lookup"><span data-stu-id="5816c-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="5816c-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5816c-125">Return value</span></span>

<span data-ttu-id="5816c-126">Тип: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5816c-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5816c-127">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="5816c-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="5816c-128">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5816c-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5816c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5816c-129">Remarks</span></span>

<span data-ttu-id="5816c-130">API Graph оператора Директмл предоставляет абстрактный способ эффективного использования Директмл в различных аппаратных средствах.</span><span class="sxs-lookup"><span data-stu-id="5816c-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="5816c-131">Директмл применяет оптимизацию на уровне тензорные, например, выбор наиболее эффективного макета тензорные в зависимости от используемого адаптера.</span><span class="sxs-lookup"><span data-stu-id="5816c-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="5816c-132">Он также применяет оптимизацию, например удаление операторов JOIN или Split.</span><span class="sxs-lookup"><span data-stu-id="5816c-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="5816c-133">Перед созданием графа Директмл рекомендуется применить высокоуровневые оптимизации.</span><span class="sxs-lookup"><span data-stu-id="5816c-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="5816c-134">Например, отказывается от операторов свертки с Батчнорм, сворачиванием констант и общим исключением части выражения.</span><span class="sxs-lookup"><span data-stu-id="5816c-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="5816c-135">Оптимизация в оптимизаторе графов Директмл предназначена для дополнения таких независимых от устройств оптимизаций, которые обычно обрабатываются универсальными платформами машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="5816c-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="5816c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="5816c-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5816c-137">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="5816c-137">**Target Platform**</span></span> | <span data-ttu-id="5816c-138">Windows</span><span class="sxs-lookup"><span data-stu-id="5816c-138">Windows</span></span> |
| <span data-ttu-id="5816c-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="5816c-139">**Header**</span></span> | <span data-ttu-id="5816c-140">директмл. h</span><span class="sxs-lookup"><span data-stu-id="5816c-140">directml.h</span></span> |
| <span data-ttu-id="5816c-141">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="5816c-141">**Library**</span></span> | <span data-ttu-id="5816c-142">Директмл. lib</span><span class="sxs-lookup"><span data-stu-id="5816c-142">DirectML.lib</span></span> |
| <span data-ttu-id="5816c-143">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="5816c-143">**DLL**</span></span> | <span data-ttu-id="5816c-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="5816c-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="5816c-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5816c-145">See also</span></span>

[<span data-ttu-id="5816c-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="5816c-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)