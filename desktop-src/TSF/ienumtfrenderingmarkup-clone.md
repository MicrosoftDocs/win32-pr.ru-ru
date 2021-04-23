---
title: Метод Clone Иенумтфрендерингмаркуп
description: Метод Clone Иенумтфрендерингмаркуп создает копию объекта перечислителя.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Платформа текстовых служб метода клонирования
- Платформа текстовых служб метода клонирования, интерфейс Иенумтфрендерингмаркуп
- Платформа текстовых служб с интерфейсом Иенумтфрендерингмаркуп, метод Clone
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681644"
---
# <a name="ienumtfrenderingmarkupclone-method"></a><span data-ttu-id="9c5bc-106">Метод Иенумтфрендерингмаркуп:: Clone</span><span class="sxs-lookup"><span data-stu-id="9c5bc-106">IEnumTfRenderingMarkup::Clone method</span></span>

<span data-ttu-id="9c5bc-107">Метод **иенумтфрендерингмаркуп:: Clone** создает копию объекта перечислителя.</span><span class="sxs-lookup"><span data-stu-id="9c5bc-107">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c5bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c5bc-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="9c5bc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c5bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c5bc-110">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9c5bc-110">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c5bc-111">\[\]указатель на интерфейс [иенумтфрендерингмаркуп](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="9c5bc-111">\[out\] A pointer to a [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c5bc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c5bc-112">Return value</span></span>

<span data-ttu-id="9c5bc-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="9c5bc-113">This method can return one of these values.</span></span>



| <span data-ttu-id="9c5bc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9c5bc-114">Value</span></span>                                                                                        | <span data-ttu-id="9c5bc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9c5bc-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9c5bc-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9c5bc-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9c5bc-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9c5bc-117">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="9c5bc-118"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="9c5bc-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="9c5bc-119">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="9c5bc-119">An unspecified error occurred.</span></span><br/>      |
| <dl> <span data-ttu-id="9c5bc-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9c5bc-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9c5bc-121">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="9c5bc-121">One or more parameters are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c5bc-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c5bc-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9c5bc-123">Этот метод в настоящее время не находится в файлах общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="9c5bc-123">This method is not currently in the public header files.</span></span> <span data-ttu-id="9c5bc-124">Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="9c5bc-124">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

