---
description: Указывает, должен ли кодировщик использовать предпочтительный размер кадра, заданный в числе выборок на кадр.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Свойство MFPKEY_REQUESTING_A_FRAMESIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699262"
---
# <a name="mfpkey_requesting_a_framesize-property"></a><span data-ttu-id="1d816-103">МФПКЭЙ \_ запрашивает \_ \_ свойство фрамесизе</span><span class="sxs-lookup"><span data-stu-id="1d816-103">MFPKEY\_REQUESTING\_A\_FRAMESIZE Property</span></span>

<span data-ttu-id="1d816-104">Указывает, должен ли кодировщик использовать предпочтительный размер кадра, заданный в числе выборок на кадр.</span><span class="sxs-lookup"><span data-stu-id="1d816-104">Specifies whether the encoder should use a preferred frame size given in number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1d816-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1d816-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1d816-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="1d816-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1d816-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1d816-107">Data Type</span></span>

<span data-ttu-id="1d816-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="1d816-108">**VT\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d816-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d816-109">Remarks</span></span>

<span data-ttu-id="1d816-110">Чтобы задать предпочтительный размер кадра, задайте следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1d816-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="1d816-111">Задайте **для \_ мфпкэй \_ запрос \_ фрамесизе** к варианту \_ true.</span><span class="sxs-lookup"><span data-stu-id="1d816-111">Set **MFPKEY\_REQUESTING\_A\_FRAMESIZE** to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="1d816-112">Задайте для параметра [**мфпкэй \_ предпочтительный \_ фрамесизе**](mfpkey-preferred-framesizeproperty.md) число выборок в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1d816-112">Set [**MFPKEY\_PREFERRED\_FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d816-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1d816-113">Requirements</span></span>



| <span data-ttu-id="1d816-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1d816-114">Requirement</span></span> | <span data-ttu-id="1d816-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1d816-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d816-116">Клиент</span><span class="sxs-lookup"><span data-stu-id="1d816-116">Client</span></span><br/> | <span data-ttu-id="1d816-117">Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d816-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="1d816-118">Header</span><span class="sxs-lookup"><span data-stu-id="1d816-118">Header</span></span><br/> | <dl> <span data-ttu-id="1d816-119"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d816-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d816-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d816-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d816-121">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d816-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
