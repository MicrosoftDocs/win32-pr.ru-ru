---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Определяет, понимается ли заданное значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) операционной системой.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792180"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a><span data-ttu-id="c454a-103">Метод Идкскореадаптерлист:: Исадаптерпреференцесуппортед</span><span class="sxs-lookup"><span data-stu-id="c454a-103">IDXCoreAdapterList::IsAdapterPreferenceSupported method</span></span>

## <a name="description"></a><span data-ttu-id="c454a-104">Описание</span><span class="sxs-lookup"><span data-stu-id="c454a-104">Description</span></span>

<span data-ttu-id="c454a-105">Определяет, понимается ли указанное значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) текущей операционной системой (ОС).</span><span class="sxs-lookup"><span data-stu-id="c454a-105">Determines whether a specified [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value is understood by the current operating system (OS).</span></span> <span data-ttu-id="c454a-106">Можно вызвать **исадаптерпреференцесуппортед** перед вызовом [Идкскореадаптерлист:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="c454a-106">You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c454a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c454a-107">Syntax</span></span>

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a><span data-ttu-id="c454a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c454a-108">Parameters</span></span>

### <a name="preference"></a><span data-ttu-id="c454a-109">preference</span><span class="sxs-lookup"><span data-stu-id="c454a-109">preference</span></span>

<span data-ttu-id="c454a-110">Тип: **[дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span><span class="sxs-lookup"><span data-stu-id="c454a-110">Type: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span></span>

<span data-ttu-id="c454a-111">Значение [дкскореадаптерпреференце](./ne-dxcore_interface-dxcoreadapterpreference.md) , которое будет проверяться на наличие поддержки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c454a-111">A [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value that will be checked to see whether it's supported by the OS.</span></span>

## <a name="returns"></a><span data-ttu-id="c454a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c454a-112">Returns</span></span>

<span data-ttu-id="c454a-113">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="c454a-113">Type: **bool**</span></span>

<span data-ttu-id="c454a-114">Возвращает значение, `true` Если тип сортировки понимается текущей ОС.</span><span class="sxs-lookup"><span data-stu-id="c454a-114">Returns `true` if the sort type is understood by the current OS.</span></span> <span data-ttu-id="c454a-115">В противном случае возвращается `false`.</span><span class="sxs-lookup"><span data-stu-id="c454a-115">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="c454a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c454a-116">See also</span></span>

<span data-ttu-id="c454a-117">[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="c454a-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>