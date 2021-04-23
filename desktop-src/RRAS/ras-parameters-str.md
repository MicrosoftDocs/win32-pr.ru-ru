---
title: Структура RAS_PARAMETERS (Рассапи. h)
description: '\_Структура параметров RAS используется функцией расадминпортжетинфо для возврата имени и значения параметра носителя, связанного с портом на сервере удаленного доступа.'
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS структуры RAS_PARAMETERS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534907"
---
# <a name="ras_parameters-structure"></a><span data-ttu-id="8a50f-104">\_Структура параметров RAS</span><span class="sxs-lookup"><span data-stu-id="8a50f-104">RAS\_PARAMETERS structure</span></span>

<span data-ttu-id="8a50f-105">\[Структура **\_ параметров RAS** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="8a50f-105">\[The **RAS\_PARAMETERS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="8a50f-106">Структура **\_ параметров RAS** используется функцией [**расадминпортжетинфо**](rasadminportgetinfo.md) для возврата имени и значения параметра носителя, связанного с портом на сервере удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="8a50f-106">The **RAS\_PARAMETERS** structure is used by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to return the name and value of a media-specific parameter associated with a port on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a50f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a50f-107">Syntax</span></span>


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="8a50f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8a50f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a50f-109">**\_Ключ P**</span><span class="sxs-lookup"><span data-stu-id="8a50f-109">**P\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="8a50f-110">Указывает имя ключа, представляющего параметр, относящийся к носителю, например МАКСКОННЕКТБПС.</span><span class="sxs-lookup"><span data-stu-id="8a50f-110">Specifies the name of the key that represents the media-specific parameter, such as MAXCONNECTBPS.</span></span>

</dd> <dt>

<span data-ttu-id="8a50f-111">**\_Тип P**</span><span class="sxs-lookup"><span data-stu-id="8a50f-111">**P\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="8a50f-112">Определяет тип данных, связанных с параметром.</span><span class="sxs-lookup"><span data-stu-id="8a50f-112">Identifies the type of data associated with the parameter.</span></span> <span data-ttu-id="8a50f-113">Этот элемент может принимать одно из следующих значений из перечисления [**\_ \_ формата параметров RAS**](ras-params-format-str.md) .</span><span class="sxs-lookup"><span data-stu-id="8a50f-113">This member can be one of the following values from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration.</span></span>



| <span data-ttu-id="8a50f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8a50f-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="8a50f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8a50f-115">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <span data-ttu-id="8a50f-116"><dt>**ParamNumber**</dt></span><span class="sxs-lookup"><span data-stu-id="8a50f-116"><dt>**ParamNumber**</dt></span></span> </dl> | <span data-ttu-id="8a50f-117">Указывает, что данные, связанные с ключом, являются числом.</span><span class="sxs-lookup"><span data-stu-id="8a50f-117">Indicates that the data associated with the key is a number.</span></span><br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <span data-ttu-id="8a50f-118"><dt>**парамстринг**</dt></span><span class="sxs-lookup"><span data-stu-id="8a50f-118"><dt>**ParamString**</dt></span></span> </dl> | <span data-ttu-id="8a50f-119">Указывает, что данные, связанные с ключом, являются строкой.</span><span class="sxs-lookup"><span data-stu-id="8a50f-119">Indicates that the data associated with the key is a string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8a50f-120">**\_Атрибуты P**</span><span class="sxs-lookup"><span data-stu-id="8a50f-120">**P\_Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="8a50f-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="8a50f-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8a50f-122">**\_Значение P**</span><span class="sxs-lookup"><span data-stu-id="8a50f-122">**P\_Value**</span></span>
</dt> <dd>

<span data-ttu-id="8a50f-123">Указывает значение, связанное с параметром.</span><span class="sxs-lookup"><span data-stu-id="8a50f-123">Specifies the value associated with the parameter.</span></span> <span data-ttu-id="8a50f-124">Этот член является объединением [**\_ \_ значений params в службе RAS**](ras-params-value-str.md) .</span><span class="sxs-lookup"><span data-stu-id="8a50f-124">This member is a [**RAS\_PARAMS\_VALUE**](ras-params-value-str.md) union.</span></span> <span data-ttu-id="8a50f-125">Если элемент **P \_ Type** имеет значение парамнумбер, то элемент **Number** в объединении содержит значения.</span><span class="sxs-lookup"><span data-stu-id="8a50f-125">If the **P\_Type** member is ParamNumber, the **Number** member of the union contains the value.</span></span> <span data-ttu-id="8a50f-126">Если **\_ тип P** — Парамстринг, то **строковый** элемент объединения содержит значение.</span><span class="sxs-lookup"><span data-stu-id="8a50f-126">If **P\_Type** is ParamString, the **String** member of the union contains the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a50f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8a50f-127">Requirements</span></span>



| <span data-ttu-id="8a50f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8a50f-128">Requirement</span></span> | <span data-ttu-id="8a50f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8a50f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a50f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a50f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8a50f-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a50f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8a50f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a50f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8a50f-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a50f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8a50f-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8a50f-134">End of client support</span></span><br/>    | <span data-ttu-id="8a50f-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a50f-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="8a50f-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8a50f-136">End of server support</span></span><br/>    | <span data-ttu-id="8a50f-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a50f-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8a50f-138">Header</span><span class="sxs-lookup"><span data-stu-id="8a50f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a50f-139"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a50f-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a50f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a50f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a50f-141">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="8a50f-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="8a50f-142">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="8a50f-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="8a50f-143">**расадминакцептневконнектион**</span><span class="sxs-lookup"><span data-stu-id="8a50f-143">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="8a50f-144">**расадминконнектионхангупнотификатион**</span><span class="sxs-lookup"><span data-stu-id="8a50f-144">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="8a50f-145">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="8a50f-145">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





