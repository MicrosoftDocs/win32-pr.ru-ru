---
title: Структура WMDM_PROP_VALUES_ENUM
description: '\_ \_ Структура перечисления значений Prop вмдм \_ содержит перечислимый набор допустимых значений для конкретного свойства в определенной конфигурации свойства.'
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694644"
---
# <a name="wmdm_prop_values_enum-structure"></a><span data-ttu-id="50b0f-104">\_ \_ Структура перечисления значений Prop вмдм \_</span><span class="sxs-lookup"><span data-stu-id="50b0f-104">WMDM\_PROP\_VALUES\_ENUM structure</span></span>

<span data-ttu-id="50b0f-105">Структура **\_ \_ \_ перечисления значений Prop вмдм** содержит перечислимый набор допустимых значений для конкретного свойства в определенной конфигурации свойства.</span><span class="sxs-lookup"><span data-stu-id="50b0f-105">The **WMDM\_PROP\_VALUES\_ENUM** structure contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b0f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50b0f-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a><span data-ttu-id="50b0f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="50b0f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="50b0f-108">**ценумвалуес**</span><span class="sxs-lookup"><span data-stu-id="50b0f-108">**cEnumValues**</span></span>
</dt> <dd>

<span data-ttu-id="50b0f-109">Число перечисляемых значений.</span><span class="sxs-lookup"><span data-stu-id="50b0f-109">Count of enumerated values.</span></span>

</dd> <dt>

<span data-ttu-id="50b0f-110">**пвалуес**</span><span class="sxs-lookup"><span data-stu-id="50b0f-110">**pValues**</span></span>
</dt> <dd>

<span data-ttu-id="50b0f-111">Указатель на массив значений.</span><span class="sxs-lookup"><span data-stu-id="50b0f-111">Pointer to an array of values.</span></span> <span data-ttu-id="50b0f-112">Размер массива равен значению параметра **ценумвалуес**.</span><span class="sxs-lookup"><span data-stu-id="50b0f-112">The size of the array is equal to the value of **cEnumValues**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50b0f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50b0f-113">Remarks</span></span>

<span data-ttu-id="50b0f-114">Эта структура используется в структуре **вмдм \_ prop \_** Structure для описания перечислимого набора допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="50b0f-114">This structure is used in the **WMDM\_PROP\_DESC** structure to describe an enumerated set of valid values.</span></span> <span data-ttu-id="50b0f-115">Перечислимый набор допустимых значений применим, если выбрано перечисление \_ \_ \_ допустимых значений Prop enum вмдм \_ \_ из перечисления **\_ \_ \_ допустимых \_ значений \_ Свойства вмдм enum Prop** .</span><span class="sxs-lookup"><span data-stu-id="50b0f-115">An enumerated set of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration.</span></span>

<span data-ttu-id="50b0f-116">Вызывающий объект необходим для высвобождения памяти, используемой **пвалуес**.</span><span class="sxs-lookup"><span data-stu-id="50b0f-116">The caller is required to free the memory used by **pValues**.</span></span> <span data-ttu-id="50b0f-117">Пример того, как это сделать, см. в [**разделе \_ \_ функция форматирования вмдм**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="50b0f-117">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50b0f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="50b0f-118">Requirements</span></span>



| <span data-ttu-id="50b0f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="50b0f-119">Requirement</span></span> | <span data-ttu-id="50b0f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="50b0f-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50b0f-121">Header</span><span class="sxs-lookup"><span data-stu-id="50b0f-121">Header</span></span><br/> | <dl> <span data-ttu-id="50b0f-122"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50b0f-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b0f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50b0f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b0f-124">**IWMDMDevice3:: Жетформаткапабилити**</span><span class="sxs-lookup"><span data-stu-id="50b0f-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="50b0f-125">**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**</span><span class="sxs-lookup"><span data-stu-id="50b0f-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="50b0f-126">**\_возможность форматирования \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="50b0f-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="50b0f-127">**\_Конфигурация вмдм Prop \_**</span><span class="sxs-lookup"><span data-stu-id="50b0f-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="50b0f-128">**ВМДМ \_ prop, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="50b0f-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="50b0f-129">**\_ \_ диапазон значений Prop \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="50b0f-129">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="50b0f-130">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="50b0f-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





