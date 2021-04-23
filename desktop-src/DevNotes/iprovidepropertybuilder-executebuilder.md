---
description: Уведомляет объект о том, что он должен отобразить его построитель для указанного свойства.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Метод Ипровидепропертибуилдер:: Ексекутебуилдер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648001"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a><span data-ttu-id="ee084-103">Метод Ипровидепропертибуилдер:: Ексекутебуилдер</span><span class="sxs-lookup"><span data-stu-id="ee084-103">IProvidePropertyBuilder::ExecuteBuilder method</span></span>

<span data-ttu-id="ee084-104">Уведомляет объект о том, что он должен отобразить его построитель для указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="ee084-104">Notifies an object that it should display its builder for the specified property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee084-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee084-105">Syntax</span></span>


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a><span data-ttu-id="ee084-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee084-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee084-107">*идентификатор DISPID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee084-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee084-108">DISPID свойства, для которого отображается конструктор.</span><span class="sxs-lookup"><span data-stu-id="ee084-108">The DISPID of the property for which the builder displays.</span></span>

</dd> <dt>

<span data-ttu-id="ee084-109">*бстргуидблдр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee084-109">*bstrGuidBldr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee084-110">Значение **BSTR** СОЗДАВАЕМОГО идентификатора GUID построителя.</span><span class="sxs-lookup"><span data-stu-id="ee084-110">The **BSTR** of the builder GUID to invoke.</span></span> <span data-ttu-id="ee084-111">Возвращается из [**маптопропертибуилдер**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="ee084-111">This is returned from [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee084-112">*пдиспапп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee084-112">*pdispApp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee084-113">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ee084-113">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ee084-114">*хвндблдровнер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee084-114">*hwndBldrOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee084-115">Маркер родительского всплывающего окна построителя.</span><span class="sxs-lookup"><span data-stu-id="ee084-115">A handle to the parent pop-up builder window.</span></span>

</dd> <dt>

<span data-ttu-id="ee084-116">*сервер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ee084-116">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee084-117">Текущее значение свойства.</span><span class="sxs-lookup"><span data-stu-id="ee084-117">The current value of the property.</span></span> <span data-ttu-id="ee084-118">Это значение может быть изменено объектом и меняется на новое значение, если *пбактионкоммиттед* имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ee084-118">This value can be modified by the object and changes to the new value if *pbActionCommitted* is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ee084-119">*пбактионкоммиттед* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ee084-119">*pbActionCommitted* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ee084-120">Значение, указывающее, выполнил ли построитель действие над объектом.</span><span class="sxs-lookup"><span data-stu-id="ee084-120">A value that indicates whether the builder performed an action on the object.</span></span> <span data-ttu-id="ee084-121">Может использоваться, когда пользователь изменяет что-либо, а затем нажимает кнопку ОК во всплывающем диалоговом окне построителя.</span><span class="sxs-lookup"><span data-stu-id="ee084-121">Can be used when a user modifies something, then presses OK on the pop-up builder dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee084-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee084-122">Return value</span></span>

<span data-ttu-id="ee084-123">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee084-123">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee084-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ee084-124">Requirements</span></span>



| <span data-ttu-id="ee084-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ee084-125">Requirement</span></span> | <span data-ttu-id="ee084-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ee084-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee084-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ee084-127">DLL</span></span><br/> | <dl> <span data-ttu-id="ee084-128"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee084-128"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee084-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee084-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee084-130">**ипровидепропертибуилдер**</span><span class="sxs-lookup"><span data-stu-id="ee084-130">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




