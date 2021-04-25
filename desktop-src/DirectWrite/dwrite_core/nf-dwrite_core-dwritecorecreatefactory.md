---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: Двритекорекреатефактори (dwrite_core. h)
description: Создает объект фабрики, который используется для последующего создания отдельных объектов Двритекоре.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 43e43e00385e10f0da0ba459cdc16e84562b72ec
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955027"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="ff7f2-103">Функция Двритекорекреатефактори (dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="ff7f2-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="ff7f2-104">Создает объект фабрики, который используется для последующего создания отдельных объектов Двритекоре.</span><span class="sxs-lookup"><span data-stu-id="ff7f2-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff7f2-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ff7f2-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="ff7f2-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="ff7f2-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="ff7f2-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/directwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="ff7f2-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff7f2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff7f2-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="ff7f2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff7f2-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="ff7f2-110">Тип: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="ff7f2-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="ff7f2-111">Значение типа, указывающее, будет ли объект фабрики общим, изолированным или ограниченным.</span><span class="sxs-lookup"><span data-stu-id="ff7f2-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="ff7f2-112">Тип: <b>рефиид</b></span><span class="sxs-lookup"><span data-stu-id="ff7f2-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="ff7f2-113">Значение идентификатора GUID, идентифицирующее интерфейс фабрики DirectWrite, например __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">идвритефактори</a>).</span><span class="sxs-lookup"><span data-stu-id="ff7f2-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="ff7f2-114">Тип: <b>IUnknown \* \*</b> .</span><span class="sxs-lookup"><span data-stu-id="ff7f2-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="ff7f2-115">Адрес указателя на вновь созданный объект фабрики DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ff7f2-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff7f2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff7f2-116">Return value</span></span>

<span data-ttu-id="ff7f2-117">Тип: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="ff7f2-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="ff7f2-118">Если этот метод завершается с ошибкой, возвращается <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="ff7f2-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="ff7f2-119">В противном случае возвращается код ошибки <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="ff7f2-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="ff7f2-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="ff7f2-120">Examples</span></span>

<span data-ttu-id="ff7f2-121">См. раздел [Обзор двритекоре](/windows/win32/directwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="ff7f2-121">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff7f2-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff7f2-122">Remarks</span></span>

<span data-ttu-id="ff7f2-123">Это функционально аналогично функции [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , экспортируемой системной версией DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ff7f2-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="ff7f2-124">Функция Двритекоре имеет другое имя, чтобы избежать неоднозначности.</span><span class="sxs-lookup"><span data-stu-id="ff7f2-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff7f2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ff7f2-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ff7f2-126">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="ff7f2-126">**Minimum supported client**</span></span> | <span data-ttu-id="ff7f2-127">Windows 10, переобъединение проектов [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="ff7f2-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="ff7f2-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="ff7f2-128">**Header**</span></span> | <span data-ttu-id="ff7f2-129">дврите. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="ff7f2-129">dwrite.h (include dwrite_core.h)</span></span> |
