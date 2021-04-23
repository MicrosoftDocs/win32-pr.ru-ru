---
description: Указывает, должен ли кодировщик проверять согласованность данных между проходами при выполнении двусторонней кодировки VBR. Чтение и запись.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Свойство MFPKEY_CHECKDATACONSISTENCY2P (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694532"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a><span data-ttu-id="d6461-104">МФПКЭЙ \_ CHECKDATACONSISTENCY2P, свойство</span><span class="sxs-lookup"><span data-stu-id="d6461-104">MFPKEY\_CHECKDATACONSISTENCY2P Property</span></span>

<span data-ttu-id="d6461-105">Указывает, должен ли кодировщик проверять согласованность данных между проходами при выполнении двусторонней кодировки VBR.</span><span class="sxs-lookup"><span data-stu-id="d6461-105">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <span data-ttu-id="d6461-106">Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="d6461-106">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d6461-107">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="d6461-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="d6461-108">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d6461-108">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d6461-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6461-109">Data Type</span></span>

<span data-ttu-id="d6461-110">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="d6461-110">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="d6461-111">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d6461-111">Default Value</span></span>

<span data-ttu-id="d6461-112">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="d6461-112">**VARIANT\_TRUE**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6461-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6461-113">Remarks</span></span>

<span data-ttu-id="d6461-114">Если оставить это свойство по умолчанию со значением **Variant \_ true**, кодировщик проверяет соответствие входных выборок между двумя проходами и завершается ошибкой, если обнаруживает несоответствие.</span><span class="sxs-lookup"><span data-stu-id="d6461-114">If you leave this property at its default value of **VARIANT\_TRUE**, the encoder verifies that the input samples match between the two passes, and fails if it detects a discrepancy.</span></span> <span data-ttu-id="d6461-115">Основной сценарий, который приводит к несоответствию, заключается в том, что входные данные поступают с устройства.</span><span class="sxs-lookup"><span data-stu-id="d6461-115">The main scenario that leads to a discrepancy is when the input comes from a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6461-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d6461-116">Requirements</span></span>



| <span data-ttu-id="d6461-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d6461-117">Requirement</span></span> | <span data-ttu-id="d6461-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d6461-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6461-119">Клиент</span><span class="sxs-lookup"><span data-stu-id="d6461-119">Client</span></span><br/> | <span data-ttu-id="d6461-120">Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6461-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="d6461-121">Header</span><span class="sxs-lookup"><span data-stu-id="d6461-121">Header</span></span><br/> | <dl> <span data-ttu-id="d6461-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6461-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6461-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6461-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6461-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6461-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
