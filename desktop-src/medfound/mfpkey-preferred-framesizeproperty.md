---
description: Указывает предпочтительное количество выборок на кадр.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Свойство MFPKEY_PREFERRED_FRAMESIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699151"
---
# <a name="mfpkey_preferred_framesize-property"></a><span data-ttu-id="85062-103">МФПКЭЙ \_ предпочтительное \_ свойство фрамесизе</span><span class="sxs-lookup"><span data-stu-id="85062-103">MFPKEY\_PREFERRED\_FRAMESIZE Property</span></span>

<span data-ttu-id="85062-104">Указывает предпочтительное количество выборок на кадр.</span><span class="sxs-lookup"><span data-stu-id="85062-104">Specifies the preferred number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="85062-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="85062-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="85062-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="85062-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="85062-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="85062-107">Data Type</span></span>

<span data-ttu-id="85062-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="85062-108">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="85062-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85062-109">Remarks</span></span>

<span data-ttu-id="85062-110">Чтобы задать предпочтительный размер кадра, задайте следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="85062-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="85062-111">Задайте [**для \_ мфпкэй \_ запрос \_ фрамесизе**](mfpkey-requesting-a-framesizeproperty.md) к **варианту \_ true**.</span><span class="sxs-lookup"><span data-stu-id="85062-111">Set [**MFPKEY\_REQUESTING\_A\_FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="85062-112">Задайте для параметра **мфпкэй \_ предпочтительный \_ фрамесизе** число выборок в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="85062-112">Set **MFPKEY\_PREFERRED\_FRAMESIZE** to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="85062-113">Требования</span><span class="sxs-lookup"><span data-stu-id="85062-113">Requirements</span></span>



| <span data-ttu-id="85062-114">Требование</span><span class="sxs-lookup"><span data-stu-id="85062-114">Requirement</span></span> | <span data-ttu-id="85062-115">Значение</span><span class="sxs-lookup"><span data-stu-id="85062-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85062-116">Клиент</span><span class="sxs-lookup"><span data-stu-id="85062-116">Client</span></span><br/> | <span data-ttu-id="85062-117">Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="85062-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="85062-118">Header</span><span class="sxs-lookup"><span data-stu-id="85062-118">Header</span></span><br/> | <dl> <span data-ttu-id="85062-119"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="85062-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85062-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85062-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85062-121">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85062-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
