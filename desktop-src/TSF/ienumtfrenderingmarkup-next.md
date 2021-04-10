---
title: Иенумтфрендерингмаркуп следующий метод
description: Следующий метод Иенумтфрендерингмаркуп получает от текущей позицией указанное число элементов в последовательности перечисления.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Платформа текстовых служб следующего метода
- Платформа текстовых служб следующего метода, интерфейс Иенумтфрендерингмаркуп
- Платформа текстовых служб с интерфейсом Иенумтфрендерингмаркуп, метод Next
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070253"
---
# <a name="ienumtfrenderingmarkupnext-method"></a><span data-ttu-id="7f0f9-106">Метод Иенумтфрендерингмаркуп:: Next</span><span class="sxs-lookup"><span data-stu-id="7f0f9-106">IEnumTfRenderingMarkup::Next method</span></span>

<span data-ttu-id="7f0f9-107">Метод **иенумтфрендерингмаркуп:: Next** получает от текущей позицией указанное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-107">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0f9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f0f9-108">Syntax</span></span>


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="7f0f9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f0f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f0f9-110">*улкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f0f9-110">*ulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f0f9-111">\[out \] указывает количество элементов для получения.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-111">\[out\] Specifies the number of elements to obtain.</span></span>

</dd> <dt>

<span data-ttu-id="7f0f9-112">*ппелемент* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f0f9-112">*ppElement* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f0f9-113">\[\]указатель out на массив структур [tf \_ рендерингмаркуп](/windows/desktop/TSF/tf-renderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="7f0f9-113">\[out\] Pointer to an array of [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) structures.</span></span> <span data-ttu-id="7f0f9-114">Этот массив должен содержать по крайней мере *улкаунт* элементов в размере.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-114">This array must be at least *ulCount* elements in size.</span></span>

</dd> <dt>

<span data-ttu-id="7f0f9-115">*пкфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f0f9-115">*pcFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f0f9-116">\[\]указатель out на значение ulong, получающее число фактически полученных элементов.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-116">\[out\] Pointer to a ULONG value that receives the number of elements actually obtained.</span></span> <span data-ttu-id="7f0f9-117">Это значение может быть меньше запрошенного количества элементов.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-117">This value can be less than the number of items requested.</span></span> <span data-ttu-id="7f0f9-118">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-118">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f0f9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f0f9-119">Return value</span></span>

<span data-ttu-id="7f0f9-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-120">This method can return one of these values.</span></span>



| <span data-ttu-id="7f0f9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7f0f9-121">Value</span></span>                                                                                        | <span data-ttu-id="7f0f9-122">Описание</span><span class="sxs-lookup"><span data-stu-id="7f0f9-122">Description</span></span>                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f0f9-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7f0f9-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7f0f9-124">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-124">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="7f0f9-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7f0f9-125"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="7f0f9-126">Метод достиг конца перечисления до получения указанного числа элементов.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-126">The method reached the end of the enumeration before the specified number of elements could be obtained.</span></span><br/> |
| <dl> <span data-ttu-id="7f0f9-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7f0f9-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7f0f9-128">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-128">One or more parameters are invalid.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="7f0f9-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f0f9-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f0f9-130">Этот метод в настоящее время не находится в файлах общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-130">This method is not currently in the public header files.</span></span> <span data-ttu-id="7f0f9-131">Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-131">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

