---
description: Обратный вызов для возврата данных таблицы объектов.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Иобжекттаблекаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4535164048c92e6af381d15ee388212fdc72da4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140687"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span data-ttu-id="7d223-103"><span id="vspixengine.iobjecttablecallback"></span>Интерфейс Иобжекттаблекаллбакк</span><span class="sxs-lookup"><span data-stu-id="7d223-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback interface</span></span>

<span data-ttu-id="7d223-104">Обратный вызов для возврата данных таблицы объектов.</span><span class="sxs-lookup"><span data-stu-id="7d223-104">Callback to return object table data.</span></span>

## <a name="members"></a><span data-ttu-id="7d223-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="7d223-105">Members</span></span>

<span data-ttu-id="7d223-106">Интерфейс **иобжекттаблекаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7d223-106">The **IObjectTableCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7d223-107">**Иобжекттаблекаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7d223-107">**IObjectTableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="7d223-108">Методы</span><span class="sxs-lookup"><span data-stu-id="7d223-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="7d223-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="7d223-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="7d223-110">Интерфейс **иобжекттаблекаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7d223-110">The **IObjectTableCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="7d223-111">Метод</span><span class="sxs-lookup"><span data-stu-id="7d223-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="7d223-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7d223-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="7d223-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>жетсуппортедколумнс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d223-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7d223-114">Возвращает сведения о том, какие столбцы (типы данных объектов) поддерживаются таблицей объектов.</span><span class="sxs-lookup"><span data-stu-id="7d223-114">Gets information about which columns (types of object data) are supported by the object table.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="7d223-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ресулткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d223-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7d223-116">Функция обратного вызова, используемая для уведомления узла о данных таблицы объектов.</span><span class="sxs-lookup"><span data-stu-id="7d223-116">A callback function used to notify the host of object table information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="7d223-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7d223-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7d223-118">Header</span><span class="sxs-lookup"><span data-stu-id="7d223-118">Header</span></span></p></td><td><span data-ttu-id="7d223-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="7d223-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
