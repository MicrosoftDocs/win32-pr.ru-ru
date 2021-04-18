---
UID: NF:directml.DMLCreateDevice1
title: Функция DMLCreateDevice1
description: Создает устройство Директмл для данного устройства Direct3D 12.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
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
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f40c7e6aa82644b67303bc60f6a8b41fa08c6f8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719935"
---
# <a name="dmlcreatedevice1-function-directmlh"></a><span data-ttu-id="45fd0-103">Функция DMLCreateDevice1 (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="45fd0-103">DMLCreateDevice1 function (directml.h)</span></span>

<span data-ttu-id="45fd0-104">Создает устройство Директмл для данного устройства Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="45fd0-104">Creates a DirectML device for a given Direct3D 12 device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45fd0-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="45fd0-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="45fd0-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="45fd0-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45fd0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45fd0-107">Syntax</span></span>

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="45fd0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="45fd0-108">Parameters</span></span>

`d3d12Device`

<span data-ttu-id="45fd0-109">Тип: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span><span class="sxs-lookup"><span data-stu-id="45fd0-109">Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span></span>

<span data-ttu-id="45fd0-110">Указатель на [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) , представляющий устройство Direct3D 12 для создания устройства директмл.</span><span class="sxs-lookup"><span data-stu-id="45fd0-110">A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over.</span></span> <span data-ttu-id="45fd0-111">Директмл поддерживает любой уровень D3D и устройства Direct3D 12, созданные на любом адаптере, включая деформацию.</span><span class="sxs-lookup"><span data-stu-id="45fd0-111">DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP.</span></span> <span data-ttu-id="45fd0-112">Однако не все функции в Директмл могут быть доступны в зависимости от возможностей устройства Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="45fd0-112">However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device.</span></span> <span data-ttu-id="45fd0-113">Дополнительные сведения см. в разделе [идмлдевице:: чеккфеатуресуппорт](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="45fd0-113">See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.</span></span>

<span data-ttu-id="45fd0-114">Если вызов **DMLCreateDevice1** успешно выполнен, устройство директмл поддерживает строгую ссылку на устройство с Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="45fd0-114">If the call to **DMLCreateDevice1** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.</span></span>

`flags`

<span data-ttu-id="45fd0-115">Тип: <b>DML_CREATE_DEVICE_FLAGS</b></span><span class="sxs-lookup"><span data-stu-id="45fd0-115">Type: <b>DML_CREATE_DEVICE_FLAGS</b></span></span>

<span data-ttu-id="45fd0-116">Значение [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) , указывающее дополнительные параметры создания устройства.</span><span class="sxs-lookup"><span data-stu-id="45fd0-116">A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.</span></span>

`minimumFeatureLevel`

<span data-ttu-id="45fd0-117">Тип: <b>DML_FEATURE_LEVEL</b></span><span class="sxs-lookup"><span data-stu-id="45fd0-117">Type: <b>DML_FEATURE_LEVEL</b></span></span>

<span data-ttu-id="45fd0-118">Значение [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) , указывающее минимальную необходимую поддержку уровня компонента.</span><span class="sxs-lookup"><span data-stu-id="45fd0-118">A [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) value specifying the minimum feature level support required.</span></span>

<span data-ttu-id="45fd0-119">Этот параметр может быть полезен для вызывающих объектов, которым требуется определенная версия Директмл, но кто может найти вызов более старой версии Директмл.</span><span class="sxs-lookup"><span data-stu-id="45fd0-119">This parameter can be useful for callers that require a specific version of DirectML, but who may find themselves calling into an older version of DirectML.</span></span> <span data-ttu-id="45fd0-120">Это может произойти, например, когда пользователь запускает приложение в более старой версии Windows 10.</span><span class="sxs-lookup"><span data-stu-id="45fd0-120">This can happen, for example, when the user runs your application on an older version of Windows 10.</span></span>

<span data-ttu-id="45fd0-121">Приложения, которые явно зависят от функциональных возможностей, представленных на определенном уровне функций, могут указывать его как *минимумфеатурелевел*.</span><span class="sxs-lookup"><span data-stu-id="45fd0-121">Applications that explicitly depend on functionality introduced in a particular feature level can specify it as a *minimumFeatureLevel*.</span></span> <span data-ttu-id="45fd0-122">Это гарантирует, что **DMLCreateDevice1** не будет выполняться, пока базовая реализация *не будет* такой же, как и требуемый минимальный уровень функций.</span><span class="sxs-lookup"><span data-stu-id="45fd0-122">This will guarantee that **DMLCreateDevice1** won't succeed unless the underlying implementation is *at least* as capable as this requested minimum feature level.</span></span>

<span data-ttu-id="45fd0-123">Обратите внимание, что, поскольку этот параметр указывает *Минимальный* уровень компонента, базовое устройство директмл может поддерживать более высокий уровень функций, чем запрошенный минимум.</span><span class="sxs-lookup"><span data-stu-id="45fd0-123">Note that as this parameter specifies a *minimum* feature level, the underlying DirectML device may in fact support a higher feature level than the requested minimum.</span></span> <span data-ttu-id="45fd0-124">После завершения создания устройства можно запросить все уровни функций, поддерживаемые этим устройством, с помощью [идмлдевице:: чеккфеатуресуппорт](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="45fd0-124">Once device creation succeeds, you can query all of the feature levels supported by this device using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span></span>

`riid`

<span data-ttu-id="45fd0-125">Тип: <b>рефиид</b></span><span class="sxs-lookup"><span data-stu-id="45fd0-125">Type: <b>REFIID</b></span></span>

<span data-ttu-id="45fd0-126">Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть на <i>устройстве</i>.</span><span class="sxs-lookup"><span data-stu-id="45fd0-126">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>.</span></span> <span data-ttu-id="45fd0-127">Это должен быть идентификатор GUID [идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="45fd0-127">This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

`ppv`

<span data-ttu-id="45fd0-128">Тип: \_ COM \_ аутптр \_ OPT \_ <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="45fd0-128">Type: \_COM\_Outptr\_opt\_ <b>void\*\*</b></span></span>

<span data-ttu-id="45fd0-129">Указатель на блок памяти, который получает указатель на устройство.</span><span class="sxs-lookup"><span data-stu-id="45fd0-129">A pointer to a memory block that receives a pointer to the device.</span></span> <span data-ttu-id="45fd0-130">Это адрес указателя на [идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice), представляющий созданное устройство директмл.</span><span class="sxs-lookup"><span data-stu-id="45fd0-130">This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.</span></span>


## <a name="return-value"></a><span data-ttu-id="45fd0-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45fd0-131">Return value</span></span>

<span data-ttu-id="45fd0-132">Тип: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="45fd0-132">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="45fd0-133">Если функция завершается с ошибкой, она возвращает <b>S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="45fd0-133">If the function succeeds, it returns <b>S_OK</b>.</span></span> <span data-ttu-id="45fd0-134">В противном случае возвращается код ошибки [HRESULT](/windows/desktop/winprog/windows-data-types) .</span><span class="sxs-lookup"><span data-stu-id="45fd0-134">Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.</span></span>

<span data-ttu-id="45fd0-135">Если эта версия Директмл не поддерживает запрашиваемый *минимумфеатурелевел* , эта функция возвратит **DXGI_ERROR_UNSUPPORTED**.</span><span class="sxs-lookup"><span data-stu-id="45fd0-135">If this version of DirectML doesn't support the *minimumFeatureLevel* requested, then this function will return **DXGI_ERROR_UNSUPPORTED**.</span></span>

<span data-ttu-id="45fd0-136">Для использования отладочных слоев Директмл необходимо установить компонент "графические инструменты" по запросу (FOD).</span><span class="sxs-lookup"><span data-stu-id="45fd0-136">The Graphics Tools Feature on Demand (FOD) must be installed in order to use the DirectML debug layers.</span></span> <span data-ttu-id="45fd0-137">Если флаг [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) указан в параметре *flags* и отладочные слои не установлены, **DMLCreateDevice1** возвращает **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span><span class="sxs-lookup"><span data-stu-id="45fd0-137">If the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag is specified in *flags* and the debug layers are not installed, then **DMLCreateDevice1** returns **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span></span>

## <a name="remarks"></a><span data-ttu-id="45fd0-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45fd0-138">Remarks</span></span>

<span data-ttu-id="45fd0-139">Более новая версия этой функции, [DMLCreateDevice1](), появилась в директмл версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="45fd0-139">A newer version of this function, [DMLCreateDevice1](), was introduced in DirectML version 1.1.0.</span></span> <span data-ttu-id="45fd0-140">**DMLCreateDevice1** эквивалентен вызову **DMLCreateDevice1** и указанию *минимумфеатурелевел* [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span><span class="sxs-lookup"><span data-stu-id="45fd0-140">**DMLCreateDevice1** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span></span>

## <a name="availability"></a><span data-ttu-id="45fd0-141">Доступность</span><span class="sxs-lookup"><span data-stu-id="45fd0-141">Availability</span></span>

<span data-ttu-id="45fd0-142">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="45fd0-142">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fd0-143">Требования</span><span class="sxs-lookup"><span data-stu-id="45fd0-143">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="45fd0-144">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="45fd0-144">**Target Platform**</span></span> | <span data-ttu-id="45fd0-145">Windows</span><span class="sxs-lookup"><span data-stu-id="45fd0-145">Windows</span></span> |
| <span data-ttu-id="45fd0-146">**Header**</span><span class="sxs-lookup"><span data-stu-id="45fd0-146">**Header**</span></span> | <span data-ttu-id="45fd0-147">директмл. h</span><span class="sxs-lookup"><span data-stu-id="45fd0-147">directml.h</span></span> |
| <span data-ttu-id="45fd0-148">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="45fd0-148">**Library**</span></span> | <span data-ttu-id="45fd0-149">Директмл. lib</span><span class="sxs-lookup"><span data-stu-id="45fd0-149">DirectML.lib</span></span> |
| <span data-ttu-id="45fd0-150">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="45fd0-150">**DLL**</span></span> | <span data-ttu-id="45fd0-151">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="45fd0-151">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="45fd0-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45fd0-152">See also</span></span>

* [<span data-ttu-id="45fd0-153">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="45fd0-153">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="45fd0-154">Журнал версий DirectML</span><span class="sxs-lookup"><span data-stu-id="45fd0-154">DirectML version history</span></span>](../dml-version-history.md)
* [<span data-ttu-id="45fd0-155">Журнал уровня компонентов DirectML</span><span class="sxs-lookup"><span data-stu-id="45fd0-155">DirectML feature level history</span></span>](/windows/win32/direct3d12/dml-feature_level-history)    
* [<span data-ttu-id="45fd0-156">Использование слоя отладки Директмл</span><span class="sxs-lookup"><span data-stu-id="45fd0-156">Using the DirectML debug layer</span></span>](../dml-debug-layer.md)