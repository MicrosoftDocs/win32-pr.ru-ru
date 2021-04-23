---
description: Примечание. Этот интерфейс не рекомендуется к использованию.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Интерфейс Иамфилтердата (данные о фай \_ . h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675298"
---
# <a name="iamfilterdata-interface"></a><span data-ttu-id="fceb8-103">Интерфейс Иамфилтердата</span><span class="sxs-lookup"><span data-stu-id="fceb8-103">IAMFilterData interface</span></span>

> [!Note]  
> <span data-ttu-id="fceb8-104">Этот интерфейс не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="fceb8-104">This interface has been deprecated.</span></span> <span data-ttu-id="fceb8-105">В новых приложениях вместо этого следует использовать интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="fceb8-105">New applications should use the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface instead.</span></span>

 

<span data-ttu-id="fceb8-106">`IAMFilterData`Интерфейс преобразует сведения о фильтре в Упакованные двоичные данные, которые могут храниться в реестре.</span><span class="sxs-lookup"><span data-stu-id="fceb8-106">The `IAMFilterData` interface converts filter information to packed binary data, which can be stored in the registry.</span></span> <span data-ttu-id="fceb8-107">Объект сопоставителя фильтров предоставляет этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fceb8-107">The Filter Mapper object exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="fceb8-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="fceb8-108">Members</span></span>

<span data-ttu-id="fceb8-109">Интерфейс **иамфилтердата** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fceb8-109">The **IAMFilterData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fceb8-110">**Иамфилтердата** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fceb8-110">**IAMFilterData** also has these types of members:</span></span>

-   [<span data-ttu-id="fceb8-111">Методы</span><span class="sxs-lookup"><span data-stu-id="fceb8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fceb8-112">Методы</span><span class="sxs-lookup"><span data-stu-id="fceb8-112">Methods</span></span>

<span data-ttu-id="fceb8-113">Интерфейс **иамфилтердата** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="fceb8-113">The **IAMFilterData** interface has these methods.</span></span>



| <span data-ttu-id="fceb8-114">Метод</span><span class="sxs-lookup"><span data-stu-id="fceb8-114">Method</span></span>                                                     | <span data-ttu-id="fceb8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="fceb8-115">Description</span></span>                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [<span data-ttu-id="fceb8-116">**креатефилтердата**</span><span class="sxs-lookup"><span data-stu-id="fceb8-116">**CreateFilterData**</span></span>](iamfilterdata-createfilterdata.md) | <span data-ttu-id="fceb8-117">Создает двоичные данные реестра для фильтра.</span><span class="sxs-lookup"><span data-stu-id="fceb8-117">Creates binary registry data for a filter.</span></span><br/>     |
| [<span data-ttu-id="fceb8-118">**парсефилтердата**</span><span class="sxs-lookup"><span data-stu-id="fceb8-118">**ParseFilterData**</span></span>](iamfilterdata-parsefilterdata.md)   | <span data-ttu-id="fceb8-119">Распаковать двоичные данные реестра для фильтра.</span><span class="sxs-lookup"><span data-stu-id="fceb8-119">Unpacks the binary registry data for a filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fceb8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fceb8-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fceb8-121">Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fceb8-121">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fceb8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fceb8-122">Requirements</span></span>



| <span data-ttu-id="fceb8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fceb8-123">Requirement</span></span> | <span data-ttu-id="fceb8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fceb8-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fceb8-125">Header</span><span class="sxs-lookup"><span data-stu-id="fceb8-125">Header</span></span><br/> | <dl> <span data-ttu-id="fceb8-126"><dt>\_Данные о данных. h</dt></span><span class="sxs-lookup"><span data-stu-id="fceb8-126"><dt>Fil\_data.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fceb8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fceb8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fceb8-128">Устаревшие интерфейсы</span><span class="sxs-lookup"><span data-stu-id="fceb8-128">Deprecated Interfaces</span></span>](deprecated-interfaces.md)
</dt> </dl>

 

 
