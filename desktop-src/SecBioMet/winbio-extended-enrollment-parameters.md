---
title: Структура WINBIO_EXTENDED_ENROLLMENT_PARAMETERS (Винбио \_ Adapter. h)
description: Содержит дополнительные сведения о том, что адаптеру подсистемы требуется создать шаблон регистрации.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- API структуры WINBIO_EXTENDED_ENROLLMENT_PARAMETERS биометрическая платформа Windows
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489558"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a><span data-ttu-id="e98db-105">\_ \_ Структура параметров расширенной регистрации винбио \_</span><span class="sxs-lookup"><span data-stu-id="e98db-105">WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS structure</span></span>

<span data-ttu-id="e98db-106">Структура **\_ \_ \_ параметров расширенной регистрации винбио** содержит дополнительные сведения о том, что адаптеру подсистемы требуется создать шаблон регистрации.</span><span class="sxs-lookup"><span data-stu-id="e98db-106">The **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure contains additional information that an engine adapter needs to create an enrollment template.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e98db-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="e98db-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e98db-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e98db-109">**Размер**</span><span class="sxs-lookup"><span data-stu-id="e98db-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="e98db-110">Размер (в байтах) структуры **\_ \_ \_ параметров расширенной регистрации винбио** .</span><span class="sxs-lookup"><span data-stu-id="e98db-110">The size (in bytes) of the **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e98db-111">**Подфакт**</span><span class="sxs-lookup"><span data-stu-id="e98db-111">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="e98db-112">Один из [**\_ биометрического \_ подтипа Винбио**](winbio-biometric-subtype-constants.md) содержит значения констант, которые предоставляют дополнительные сведения о регистрации.</span><span class="sxs-lookup"><span data-stu-id="e98db-112">One of the [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md) values that provides additional information about the enrollment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e98db-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e98db-113">Remarks</span></span>

<span data-ttu-id="e98db-114">Биометрическая платформа Windows передает эту структуру методу [**енгинеадаптерсетенроллментпараметерс**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) во время операции регистрации.</span><span class="sxs-lookup"><span data-stu-id="e98db-114">The Windows Biometric Framework passes this structure to the [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) method during an enrollment operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e98db-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e98db-115">Requirements</span></span>



| <span data-ttu-id="e98db-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e98db-116">Requirement</span></span> | <span data-ttu-id="e98db-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e98db-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e98db-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e98db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e98db-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e98db-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="e98db-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e98db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e98db-121">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e98db-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="e98db-122">Header</span><span class="sxs-lookup"><span data-stu-id="e98db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e98db-123"><dt>Винбио \_ Adapter. h (включить винбио \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e98db-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





