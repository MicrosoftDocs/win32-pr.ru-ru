---
description: Сбрасывает состояние работоспособности для всех приложений в виртуальной машине.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Метод Ивмаппликатионхеалсмонитор:: Ресеталлаппликатионстате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898334"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a><span data-ttu-id="74650-103">Метод Ивмаппликатионхеалсмонитор:: Ресеталлаппликатионстате</span><span class="sxs-lookup"><span data-stu-id="74650-103">IVmApplicationHealthMonitor::ResetAllApplicationState method</span></span>

<span data-ttu-id="74650-104">Сбрасывает состояние работоспособности для всех приложений в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="74650-104">Resets the health state for all applications in a virtual machine.</span></span> <span data-ttu-id="74650-105">В случае успеха состояние работоспособности всех наблюдаемых приложений будет равно **аппликатионстатехеалси**.</span><span class="sxs-lookup"><span data-stu-id="74650-105">If successful, the health state for all monitored applications will be set to **ApplicationStateHealthy**.</span></span>

## <a name="syntax"></a><span data-ttu-id="74650-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74650-106">Syntax</span></span>


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a><span data-ttu-id="74650-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="74650-107">Parameters</span></span>

<span data-ttu-id="74650-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="74650-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74650-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74650-109">Return value</span></span>

<span data-ttu-id="74650-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="74650-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74650-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="74650-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74650-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74650-112">Remarks</span></span>

<span data-ttu-id="74650-113">Чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.</span><span class="sxs-lookup"><span data-stu-id="74650-113">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="74650-114">Требования</span><span class="sxs-lookup"><span data-stu-id="74650-114">Requirements</span></span>



| <span data-ttu-id="74650-115">Требование</span><span class="sxs-lookup"><span data-stu-id="74650-115">Requirement</span></span> | <span data-ttu-id="74650-116">Значение</span><span class="sxs-lookup"><span data-stu-id="74650-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74650-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74650-117">Minimum supported client</span></span><br/> | <span data-ttu-id="74650-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="74650-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="74650-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74650-119">Minimum supported server</span></span><br/> | <span data-ttu-id="74650-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="74650-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74650-121">Версия</span><span class="sxs-lookup"><span data-stu-id="74650-121">Version</span></span><br/>                  | <span data-ttu-id="74650-122">Компоненты интеграции для Windows 8</span><span class="sxs-lookup"><span data-stu-id="74650-122">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="74650-123">IDL</span><span class="sxs-lookup"><span data-stu-id="74650-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74650-124"><dt>Вмаппликатионхеалсмонитор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="74650-124"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74650-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74650-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74650-126">**ивмаппликатионхеалсмонитор**</span><span class="sxs-lookup"><span data-stu-id="74650-126">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




