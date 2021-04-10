---
title: Перечисление RAS_PARAMS_FORMAT (Рассапи. h)
description: '\_ \_ Тип перечисления "Параметры RAS" используется в \_ структуре параметров RAS для указания типа данных, связанных с ключом, относящимся к носителю.'
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS перечисления RAS_PARAMS_FORMAT
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136374"
---
# <a name="ras_params_format-enumeration"></a><span data-ttu-id="0f220-104">\_ \_ Перечисление форматов параметров RAS</span><span class="sxs-lookup"><span data-stu-id="0f220-104">RAS\_PARAMS\_FORMAT enumeration</span></span>

<span data-ttu-id="0f220-105">\[Перечисление **\_ \_ форматов параметров RAS** не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="0f220-105">\[The **RAS\_PARAMS\_FORMAT** enumeration is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="0f220-106">Тип перечисления "Параметры **RAS \_ \_** " используется в структуре [**\_ параметров RAS**](ras-parameters-str.md) для указания типа данных, связанных с ключом, относящимся к носителю.</span><span class="sxs-lookup"><span data-stu-id="0f220-106">The **RAS\_PARAMS\_FORMAT** enumeration type is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to indicate the type of data associated with a media-specific key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f220-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f220-107">Syntax</span></span>


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="0f220-108">Константы</span><span class="sxs-lookup"><span data-stu-id="0f220-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0f220-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**парамнумбер**</span><span class="sxs-lookup"><span data-stu-id="0f220-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0f220-110">Указывает, что данные, связанные с ключом, являются числом.</span><span class="sxs-lookup"><span data-stu-id="0f220-110">Indicates that the data associated with the key is a number.</span></span>

</dd> <dt>

<span data-ttu-id="0f220-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**парамстринг**</span><span class="sxs-lookup"><span data-stu-id="0f220-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span></span>
</dt> <dd>

<span data-ttu-id="0f220-112">Указывает, что данные, связанные с ключом, являются строкой.</span><span class="sxs-lookup"><span data-stu-id="0f220-112">Indicates that the data associated with the key is a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f220-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0f220-113">Requirements</span></span>



| <span data-ttu-id="0f220-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0f220-114">Requirement</span></span> | <span data-ttu-id="0f220-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0f220-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f220-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f220-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0f220-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f220-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0f220-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f220-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0f220-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f220-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0f220-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0f220-120">End of client support</span></span><br/>    | <span data-ttu-id="0f220-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f220-121">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="0f220-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0f220-122">End of server support</span></span><br/>    | <span data-ttu-id="0f220-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f220-123">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="0f220-124">Header</span><span class="sxs-lookup"><span data-stu-id="0f220-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f220-125"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f220-125"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f220-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f220-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f220-127">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="0f220-127">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="0f220-128">Перечисления для администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="0f220-128">RAS Server Administration Enumerations</span></span>](ras-server-administration-enumerations.md)
</dt> <dt>

[<span data-ttu-id="0f220-129">**\_Параметры RAS**</span><span class="sxs-lookup"><span data-stu-id="0f220-129">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> </dl>

 

 





