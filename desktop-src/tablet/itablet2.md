---
description: Расширяет интерфейс Итаблет.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Интерфейс ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719656"
---
# <a name="itablet2-interface"></a><span data-ttu-id="bea3b-103">Интерфейс ITablet2</span><span class="sxs-lookup"><span data-stu-id="bea3b-103">ITablet2 interface</span></span>

<span data-ttu-id="bea3b-104">Расширяет [**интерфейс итаблет**](itablet.md).</span><span class="sxs-lookup"><span data-stu-id="bea3b-104">Extends the [**ITablet Interface**](itablet.md).</span></span>

## <a name="members"></a><span data-ttu-id="bea3b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="bea3b-105">Members</span></span>

<span data-ttu-id="bea3b-106">Интерфейс **ITablet2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bea3b-106">The **ITablet2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bea3b-107">**ITablet2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bea3b-107">**ITablet2** also has these types of members:</span></span>

-   [<span data-ttu-id="bea3b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="bea3b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bea3b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="bea3b-109">Methods</span></span>

<span data-ttu-id="bea3b-110">Интерфейс **ITablet2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bea3b-110">The **ITablet2** interface has these methods.</span></span>



| <span data-ttu-id="bea3b-111">Метод</span><span class="sxs-lookup"><span data-stu-id="bea3b-111">Method</span></span>                                          | <span data-ttu-id="bea3b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bea3b-112">Description</span></span>                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bea3b-113">**жетдевицекинд**</span><span class="sxs-lookup"><span data-stu-id="bea3b-113">**GetDeviceKind**</span></span>](itablet2-getdevicekind.md) | <span data-ttu-id="bea3b-114">Возвращает тип аппаратного устройства, которое представляет объект планшета, например мышь, перо или сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="bea3b-114">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bea3b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bea3b-115">Remarks</span></span>

<span data-ttu-id="bea3b-116">Этот интерфейс появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bea3b-116">This interface was introduced in Windows Vista.</span></span>

<span data-ttu-id="bea3b-117">Разработчики не должны использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bea3b-117">Developers should not use this interface.</span></span>

<span data-ttu-id="bea3b-118">В следующем коде показано, как определяется интерфейс **ITablet2** .</span><span class="sxs-lookup"><span data-stu-id="bea3b-118">The following code describes how the **ITablet2** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a><span data-ttu-id="bea3b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bea3b-119">Requirements</span></span>



| <span data-ttu-id="bea3b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bea3b-120">Requirement</span></span> | <span data-ttu-id="bea3b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bea3b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bea3b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bea3b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bea3b-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bea3b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bea3b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bea3b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bea3b-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bea3b-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bea3b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bea3b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bea3b-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bea3b-127"><dt>Wisptis.exe</dt></span></span> </dl> |



 

