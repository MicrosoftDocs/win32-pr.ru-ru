---
description: 'Повторно создает данные о свойстве и внутренних свойствах приложения для массива байтов, созданного ранее с помощью Иконтекстноде:: Савепропертиесдата.'
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'Метод Иконтекстноде:: Лоадпропертиесдата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692436"
---
# <a name="icontextnodeloadpropertiesdata-method"></a><span data-ttu-id="cabc1-103">Метод Иконтекстноде:: Лоадпропертиесдата</span><span class="sxs-lookup"><span data-stu-id="cabc1-103">IContextNode::LoadPropertiesData method</span></span>

<span data-ttu-id="cabc1-104">Повторно создает данные о свойстве и внутренних свойствах приложения для массива байтов, созданного ранее с помощью [**иконтекстноде:: савепропертиесдата**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="cabc1-104">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cabc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cabc1-105">Syntax</span></span>


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="cabc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cabc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cabc1-107">*кбпропертиесдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cabc1-107">*cbPropertiesDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cabc1-108">Размер массива данных свойств.</span><span class="sxs-lookup"><span data-stu-id="cabc1-108">The size of the properties data array.</span></span>

</dd> <dt>

<span data-ttu-id="cabc1-109">*пбпропертиесдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cabc1-109">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cabc1-110">Массив 8-разрядных целых чисел без знака, содержащий сведения о свойствах для загрузки.</span><span class="sxs-lookup"><span data-stu-id="cabc1-110">The 8-bit unsigned integer array containing property information to load.</span></span>

</dd> <dt>

<span data-ttu-id="cabc1-111">*пфсукцессфул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cabc1-111">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cabc1-112">**Вариант \_ Значение TRUE** , если данные свойства успешно загружены; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="cabc1-112">**VARIANT\_TRUE** if the property data loaded successfully; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cabc1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cabc1-113">Return value</span></span>

<span data-ttu-id="cabc1-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cabc1-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cabc1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cabc1-115">Requirements</span></span>



| <span data-ttu-id="cabc1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cabc1-116">Requirement</span></span> | <span data-ttu-id="cabc1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cabc1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cabc1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cabc1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cabc1-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cabc1-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cabc1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cabc1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cabc1-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cabc1-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cabc1-122">Header</span><span class="sxs-lookup"><span data-stu-id="cabc1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cabc1-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cabc1-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cabc1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cabc1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cabc1-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cabc1-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cabc1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cabc1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cabc1-127">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="cabc1-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="cabc1-128">**Иконтекстноде:: Аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="cabc1-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="cabc1-129">**Иконтекстноде:: Контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="cabc1-129">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="cabc1-130">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="cabc1-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="cabc1-131">**Иконтекстноде:: Жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="cabc1-131">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="cabc1-132">**Иконтекстноде:: Ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="cabc1-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="cabc1-133">**Иконтекстноде:: Савепропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="cabc1-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="cabc1-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="cabc1-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




