---
title: Структура WMDM_PROP_DESC
description: Структура ВМДМ \_ prop \_ Structure описывает допустимые значения свойства в определенной конфигурации свойства.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699038"
---
# <a name="wmdm_prop_desc-structure"></a><span data-ttu-id="0962c-104">\_Структура вмдм Prop \_</span><span class="sxs-lookup"><span data-stu-id="0962c-104">WMDM\_PROP\_DESC structure</span></span>

<span data-ttu-id="0962c-105">Структура **вмдм \_ prop \_** Structure описывает допустимые значения свойства в определенной конфигурации свойства.</span><span class="sxs-lookup"><span data-stu-id="0962c-105">The **WMDM\_PROP\_DESC** structure describes valid values of a property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="0962c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0962c-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a><span data-ttu-id="0962c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0962c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0962c-108">**пвсзпропнаме**</span><span class="sxs-lookup"><span data-stu-id="0962c-108">**pwszPropName**</span></span>
</dt> <dd>

<span data-ttu-id="0962c-109">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="0962c-109">Name of the property.</span></span> <span data-ttu-id="0962c-110">Приложение должно освободить эту память, когда она будет создана с ее помощью.</span><span class="sxs-lookup"><span data-stu-id="0962c-110">The application must free this memory when it is done using it.</span></span>

</dd> <dt>

<span data-ttu-id="0962c-111">**валидвалуесформ**</span><span class="sxs-lookup"><span data-stu-id="0962c-111">**ValidValuesForm**</span></span>
</dt> <dd>

<span data-ttu-id="0962c-112">[**\_ \_ \_ Допустимые \_ значения \_ свойства Prop enum вмдм формируют**](wmdm-enum-prop-valid-values-form.md) значение перечисления, описывающее тип значений, например диапазон или список.</span><span class="sxs-lookup"><span data-stu-id="0962c-112">An [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration value describing the type of values, such as a range or list.</span></span> <span data-ttu-id="0962c-113">Значение этого перечисления определяет, какая переменная-член используется.</span><span class="sxs-lookup"><span data-stu-id="0962c-113">The value of this enumeration determines which member variable is used.</span></span>

</dd> <dt>

<span data-ttu-id="0962c-114">**ValidValues**</span><span class="sxs-lookup"><span data-stu-id="0962c-114">**ValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="0962c-115">Содержит допустимые значения свойства в конфигурации конкретного свойства.</span><span class="sxs-lookup"><span data-stu-id="0962c-115">Holds the valid values of the property in a particular property configuration.</span></span> <span data-ttu-id="0962c-116">Этот элемент содержит один из трех элементов: значение перечисления ВМДМ \_ Enum \_ prop \_ Допустимые \_ значения \_ any; элемент **валидвалуесранже** или элемент **енумератедвалидвалуес**.</span><span class="sxs-lookup"><span data-stu-id="0962c-116">This member holds one of three items: the enumeration value WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY; the member **ValidValuesRange**; or the member **EnumeratedValidValues**.</span></span> <span data-ttu-id="0962c-117">Значение или член обозначается **валидвалуесформ**.</span><span class="sxs-lookup"><span data-stu-id="0962c-117">The value or member is indicated by **ValidValuesForm**.</span></span>

<dl> <dt>

<span data-ttu-id="0962c-118">**валидвалуесранже**</span><span class="sxs-lookup"><span data-stu-id="0962c-118">**ValidValuesRange**</span></span>
</dt> <dd>

<span data-ttu-id="0962c-119">Структура [**\_ \_ \_ диапазона значений Prop вмдм**](wmdm-prop-values-range.md) , содержащая диапазон допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="0962c-119">A [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure containing a range of valid values.</span></span> <span data-ttu-id="0962c-120">Это происходит только в том случае, если для **валидвалуесформ** задано значение вмдм \_ Enum \_ PROPS \_ Range допустимые \_ значения \_ .</span><span class="sxs-lookup"><span data-stu-id="0962c-120">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE.</span></span> <span data-ttu-id="0962c-121">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0962c-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0962c-122">**енумератедвалидвалуес**</span><span class="sxs-lookup"><span data-stu-id="0962c-122">**EnumeratedValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="0962c-123">Структура [**\_ \_ \_ перечисления значений Prop вмдм**](wmdm-prop-values-enum.md) , содержащая перечислимый набор допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="0962c-123">A [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure containing an enumerated set of valid values.</span></span> <span data-ttu-id="0962c-124">Это происходит, только если для **валидвалуесформ** задано значение вмдм \_ Enum \_ prop \_ Values Valid \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0962c-124">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM.</span></span> <span data-ttu-id="0962c-125">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0962c-125">See Remarks.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0962c-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0962c-126">Remarks</span></span>

<span data-ttu-id="0962c-127">Структура **вмдм \_ prop \_** содержит описание свойства, состоящее из имени свойства и его допустимых значений в конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0962c-127">The **WMDM\_PROP\_DESC** structure contains a property description that consists of a property name and its valid values in a particular configuration.</span></span>

<span data-ttu-id="0962c-128">Вызывающий объект необходим для высвобождения памяти, используемой **валидвалуесранже** или **енумератедвалуес**.</span><span class="sxs-lookup"><span data-stu-id="0962c-128">The caller is required to free the memory used by **ValidValuesRange** or **EnumeratedValues**.</span></span> <span data-ttu-id="0962c-129">Пример того, как это сделать, см. в [**разделе \_ \_ функция форматирования вмдм**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="0962c-129">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0962c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="0962c-130">Requirements</span></span>



| <span data-ttu-id="0962c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="0962c-131">Requirement</span></span> | <span data-ttu-id="0962c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="0962c-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0962c-133">Header</span><span class="sxs-lookup"><span data-stu-id="0962c-133">Header</span></span><br/> | <dl> <span data-ttu-id="0962c-134"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0962c-134"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0962c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0962c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0962c-136">**IWMDMDevice3:: Жетформаткапабилити**</span><span class="sxs-lookup"><span data-stu-id="0962c-136">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="0962c-137">**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**</span><span class="sxs-lookup"><span data-stu-id="0962c-137">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="0962c-138">**\_возможность форматирования \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="0962c-138">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="0962c-139">**\_Конфигурация вмдм Prop \_**</span><span class="sxs-lookup"><span data-stu-id="0962c-139">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="0962c-140">**\_ \_ перечисление значений Prop вмдм \_**</span><span class="sxs-lookup"><span data-stu-id="0962c-140">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="0962c-141">**\_ \_ диапазон значений Prop \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="0962c-141">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="0962c-142">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="0962c-142">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





