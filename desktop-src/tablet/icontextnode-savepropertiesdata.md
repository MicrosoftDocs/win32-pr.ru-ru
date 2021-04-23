---
description: Извлекает массив байтов, содержащий данные внутреннего свойства и внутренних свойств для данного Иконтекстноде.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'Метод Иконтекстноде:: Савепропертиесдата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991161"
---
# <a name="icontextnodesavepropertiesdata-method"></a><span data-ttu-id="efb52-103">Метод Иконтекстноде:: Савепропертиесдата</span><span class="sxs-lookup"><span data-stu-id="efb52-103">IContextNode::SavePropertiesData method</span></span>

<span data-ttu-id="efb52-104">Извлекает массив байтов, содержащий данные внутреннего свойства и внутренних свойств для данного [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="efb52-104">Retrieves an array of bytes that contains the application-specific and internal property data for this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="efb52-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efb52-105">Syntax</span></span>


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="efb52-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efb52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb52-107">*пулпропертиесдатасизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="efb52-107">*pulPropertiesDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="efb52-108">Размер массива данных, содержащего сведения о свойстве.</span><span class="sxs-lookup"><span data-stu-id="efb52-108">The size of the data array containing the property information.</span></span> <span data-ttu-id="efb52-109">Переданное значение не используется.</span><span class="sxs-lookup"><span data-stu-id="efb52-109">The value passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="efb52-110">*ппбпропертиесдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="efb52-110">*ppbPropertiesData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efb52-111">Указатель на массив 8-разрядных целых чисел без знака, который содержит данные свойства и внутренних свойств для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="efb52-111">A pointer to an 8-bit unsigned integer array that contains the application-specific and internal property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb52-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efb52-112">Return value</span></span>

<span data-ttu-id="efb52-113">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="efb52-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="efb52-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efb52-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="efb52-115">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппбпропертиесдата* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="efb52-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertiesData* when you no longer need the information.</span></span>

 

<span data-ttu-id="efb52-116">Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="efb52-116">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="efb52-117">Этот метод сохраняет данные свойства, установленные **иинканализер** в [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="efb52-117">This method saves the property data that the **IInkAnalyzer** has set on the [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="efb52-118">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="efb52-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efb52-119">Требования</span><span class="sxs-lookup"><span data-stu-id="efb52-119">Requirements</span></span>



| <span data-ttu-id="efb52-120">Требование</span><span class="sxs-lookup"><span data-stu-id="efb52-120">Requirement</span></span> | <span data-ttu-id="efb52-121">Значение</span><span class="sxs-lookup"><span data-stu-id="efb52-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb52-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efb52-122">Minimum supported client</span></span><br/> | <span data-ttu-id="efb52-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="efb52-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="efb52-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efb52-124">Minimum supported server</span></span><br/> | <span data-ttu-id="efb52-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="efb52-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="efb52-126">Header</span><span class="sxs-lookup"><span data-stu-id="efb52-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="efb52-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="efb52-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="efb52-128">DLL</span><span class="sxs-lookup"><span data-stu-id="efb52-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efb52-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb52-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="efb52-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efb52-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb52-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="efb52-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="efb52-132">**Иконтекстноде:: Лоадпропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="efb52-132">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="efb52-133">**Иконтекстноде:: Аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="efb52-133">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="efb52-134">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="efb52-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="efb52-135">**Иконтекстноде:: Ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="efb52-135">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="efb52-136">**Иконтекстноде:: Жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="efb52-136">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="efb52-137">**Иконтекстноде:: Контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="efb52-137">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="efb52-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="efb52-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

