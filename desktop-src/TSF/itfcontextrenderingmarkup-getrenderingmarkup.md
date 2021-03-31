---
title: Итфконтекстрендерингмаркуп Жетрендерингмаркуп, метод
description: Метод Итфконтекстрендерингмаркуп Жетрендерингмаркуп извлекает перечислитель для разметки отрисовки для заданного диапазона.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Платформа служб текстового ввода метода Жетрендерингмаркуп
- Платформа текстовых служб метода Жетрендерингмаркуп, интерфейс Итфконтекстрендерингмаркуп
- Платформа текстовых служб интерфейса Итфконтекстрендерингмаркуп, метод Жетрендерингмаркуп
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792565"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a><span data-ttu-id="39299-106">Метод Итфконтекстрендерингмаркуп:: Жетрендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="39299-106">ITfContextRenderingMarkup::GetRenderingMarkup method</span></span>

<span data-ttu-id="39299-107">Метод **итфконтекстрендерингмаркуп:: жетрендерингмаркуп** извлекает перечислитель для разметки отрисовки для заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="39299-107">The **ITfContextRenderingMarkup::GetRenderingMarkup** method retrieves an enumerator of the rendering markups for the given range.</span></span>

## <a name="syntax"></a><span data-ttu-id="39299-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39299-108">Syntax</span></span>


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="39299-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="39299-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39299-110">*EC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39299-110">*ec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39299-111">\[в \] файле cookie редактирования только для чтения для доступа к контексту.</span><span class="sxs-lookup"><span data-stu-id="39299-111">\[in\] A read only edit cookie to access the context.</span></span>

</dd> <dt>

<span data-ttu-id="39299-112">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39299-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39299-113">\[В поле\]</span><span class="sxs-lookup"><span data-stu-id="39299-113">\[in\]</span></span>



| <span data-ttu-id="39299-114">Значение</span><span class="sxs-lookup"><span data-stu-id="39299-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="39299-115">Значение</span><span class="sxs-lookup"><span data-stu-id="39299-115">Meaning</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <span data-ttu-id="39299-116"><dt>**TF \_ ГРМ \_ include, \_ свойство**</dt></span><span class="sxs-lookup"><span data-stu-id="39299-116"><dt>**TF\_GRM\_INCLUDE\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="39299-117">Если этот бит равен 1, перечислитель будет включать в себя \_ свойство атрибута prop для GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="39299-117">If this bit is 1, the enumerator will include the GUID\_PROP\_ATTRIBUTE property.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="39299-118">*пранжековер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39299-118">*pRangeCover* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39299-119">\[в \] указателе на интерфейс [итфранже](/windows/desktop/api/Msctf/nn-msctf-itfrange) диапазона для перечисления разметки отрисовки.</span><span class="sxs-lookup"><span data-stu-id="39299-119">\[in\] A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface of the range to enumerate the rendering markups.</span></span>

</dd> <dt>

<span data-ttu-id="39299-120">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39299-120">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39299-121">\[\]указатель на получение указателя на интерфейс [иенумтфрендерингмаркуп](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="39299-121">\[out\] A pointer to retrieve [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39299-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39299-122">Return value</span></span>

<span data-ttu-id="39299-123">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="39299-123">This method can return one of these values.</span></span>



| <span data-ttu-id="39299-124">Значение</span><span class="sxs-lookup"><span data-stu-id="39299-124">Value</span></span>                                                                                | <span data-ttu-id="39299-125">Описание</span><span class="sxs-lookup"><span data-stu-id="39299-125">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="39299-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="39299-126"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="39299-127">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="39299-127">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39299-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39299-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="39299-129">Этот метод в настоящее время не находится в файлах общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="39299-129">This method is not currently in the public header files.</span></span> <span data-ttu-id="39299-130">Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="39299-130">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

