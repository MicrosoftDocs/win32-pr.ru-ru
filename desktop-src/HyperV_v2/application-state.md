---
description: Указывает состояние работоспособности приложения.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: Перечисление APPLICATION_STATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663383"
---
# <a name="application_state-enumeration"></a><span data-ttu-id="51e80-103">\_Перечисление состояния приложения</span><span class="sxs-lookup"><span data-stu-id="51e80-103">APPLICATION\_STATE enumeration</span></span>

<span data-ttu-id="51e80-104">Указывает состояние работоспособности приложения.</span><span class="sxs-lookup"><span data-stu-id="51e80-104">Specifies the health state of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51e80-105">Syntax</span></span>


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a><span data-ttu-id="51e80-106">Константы</span><span class="sxs-lookup"><span data-stu-id="51e80-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51e80-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**аппликатионстатехеалси**</span><span class="sxs-lookup"><span data-stu-id="51e80-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span></span>
</dt> <dd>

<span data-ttu-id="51e80-108">Приложение находится в работоспособном состоянии.</span><span class="sxs-lookup"><span data-stu-id="51e80-108">The application state is healthy.</span></span>

</dd> <dt>

<span data-ttu-id="51e80-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**аппликатионстатекритикал**</span><span class="sxs-lookup"><span data-stu-id="51e80-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span></span>
</dt> <dd>

<span data-ttu-id="51e80-110">Состояние приложения является критическим.</span><span class="sxs-lookup"><span data-stu-id="51e80-110">The application state is critical.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51e80-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51e80-111">Remarks</span></span>

<span data-ttu-id="51e80-112">Чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.</span><span class="sxs-lookup"><span data-stu-id="51e80-112">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e80-113">Требования</span><span class="sxs-lookup"><span data-stu-id="51e80-113">Requirements</span></span>



| <span data-ttu-id="51e80-114">Требование</span><span class="sxs-lookup"><span data-stu-id="51e80-114">Requirement</span></span> | <span data-ttu-id="51e80-115">Значение</span><span class="sxs-lookup"><span data-stu-id="51e80-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e80-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51e80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="51e80-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="51e80-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="51e80-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51e80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="51e80-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="51e80-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="51e80-120">Версия</span><span class="sxs-lookup"><span data-stu-id="51e80-120">Version</span></span><br/>                  | <span data-ttu-id="51e80-121">Компоненты интеграции для Windows 8</span><span class="sxs-lookup"><span data-stu-id="51e80-121">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="51e80-122">IDL</span><span class="sxs-lookup"><span data-stu-id="51e80-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51e80-123"><dt>Вмаппликатионхеалсмонитор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="51e80-123"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e80-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51e80-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e80-125">**сетаппликатионстате**</span><span class="sxs-lookup"><span data-stu-id="51e80-125">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




