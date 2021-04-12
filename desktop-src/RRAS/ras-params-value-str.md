---
title: Объединение RAS_PARAMS_VALUE (Рассапи. h)
description: '\_Объединение значений параметров RAS \_ используется в \_ структуре параметров RAS для хранения данных, связанных с параметром носителя.'
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS RAS_PARAMS_VALUE Union
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135066"
---
# <a name="ras_params_value-union"></a><span data-ttu-id="b8d6c-104">\_ \_ Объединение значений параметров RAS</span><span class="sxs-lookup"><span data-stu-id="b8d6c-104">RAS\_PARAMS\_VALUE union</span></span>

<span data-ttu-id="b8d6c-105">\[Объединение **\_ \_ значений параметров RAS** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="b8d6c-105">\[The **RAS\_PARAMS\_VALUE** union is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="b8d6c-106">Объединение **\_ \_ значений параметров RAS** используется в структуре [**\_ параметров RAS**](ras-parameters-str.md) для хранения данных, связанных с параметром носителя.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-106">The **RAS\_PARAMS\_VALUE** union is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to store the data associated with a media-specific parameter.</span></span> <span data-ttu-id="b8d6c-107">Член **\_ типа P** структуры **\_ параметров RAS** использует значение из перечисления [**\_ \_ форматов params RAS**](ras-params-format-str.md) для указания типа значения, хранящегося в данный момент в **\_ \_ значении параметров RAS**.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-107">The **P\_Type** member of the **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the type of value currently stored in **RAS\_PARAMS\_VALUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d6c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8d6c-108">Syntax</span></span>


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a><span data-ttu-id="b8d6c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b8d6c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b8d6c-110">**Число**</span><span class="sxs-lookup"><span data-stu-id="b8d6c-110">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="b8d6c-111">Если членом **\_ типа P** структуры [**\_ параметров RAS**](ras-parameters-str.md) является парамнумбер, то элемент **Number** содержит значение параметра, относящегося к носителю.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-111">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="b8d6c-112">Например, параметр МАКСКОННЕКТБПС имеет тип Парамнумбер, а значение может быть 19200.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-112">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

<span data-ttu-id="b8d6c-113">Если членом **\_ типа P** структуры [**\_ параметров RAS**](ras-parameters-str.md) является парамнумбер, то элемент **Number** содержит значение параметра, относящегося к носителю.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-113">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="b8d6c-114">Например, параметр МАКСКОННЕКТБПС имеет тип Парамнумбер, а значение может быть 19200.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-114">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

</dd> <dt>

<span data-ttu-id="b8d6c-115">**String**</span><span class="sxs-lookup"><span data-stu-id="b8d6c-115">**String**</span></span>
</dt> <dd>

<span data-ttu-id="b8d6c-116">Если **\_ тип P** элемента структуры [**\_ параметров RAS**](ras-parameters-str.md) — парамстринг, то **строковый** элемент содержит значение параметра, относящегося к носителю.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-116">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamString, the **String** member contains the value of the media-specific parameter.</span></span>

<dl> <dt>

<span data-ttu-id="b8d6c-117">**Длина**</span><span class="sxs-lookup"><span data-stu-id="b8d6c-117">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="b8d6c-118">Задает длину строки в символах, на которую указывает элемент **данных** .</span><span class="sxs-lookup"><span data-stu-id="b8d6c-118">Specifies the length, in characters, of the string pointed to by the **Data** member.</span></span>

</dd> <dt>

<span data-ttu-id="b8d6c-119">**Data**</span><span class="sxs-lookup"><span data-stu-id="b8d6c-119">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="b8d6c-120">Указатель на буфер, содержащий строковое значение параметра, относящегося к носителю.</span><span class="sxs-lookup"><span data-stu-id="b8d6c-120">Pointer to a buffer that contains the string value of a media-specific parameter.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8d6c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b8d6c-121">Requirements</span></span>



| <span data-ttu-id="b8d6c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b8d6c-122">Requirement</span></span> | <span data-ttu-id="b8d6c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b8d6c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d6c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8d6c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b8d6c-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8d6c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b8d6c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8d6c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b8d6c-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8d6c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8d6c-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b8d6c-128">End of client support</span></span><br/>    | <span data-ttu-id="b8d6c-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8d6c-129">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="b8d6c-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b8d6c-130">End of server support</span></span><br/>    | <span data-ttu-id="b8d6c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8d6c-131">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="b8d6c-132">Header</span><span class="sxs-lookup"><span data-stu-id="b8d6c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8d6c-133"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d6c-133"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8d6c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8d6c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d6c-135">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="b8d6c-135">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b8d6c-136">Объединение администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="b8d6c-136">RAS Server Administration Union</span></span>](ras-server-administration-union.md)
</dt> <dt>

[<span data-ttu-id="b8d6c-137">**\_Параметры RAS**</span><span class="sxs-lookup"><span data-stu-id="b8d6c-137">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="b8d6c-138">**\_Формат параметров RAS \_**</span><span class="sxs-lookup"><span data-stu-id="b8d6c-138">**RAS\_PARAMS\_FORMAT**</span></span>](ras-params-format-str.md)
</dt> </dl>

 

 





