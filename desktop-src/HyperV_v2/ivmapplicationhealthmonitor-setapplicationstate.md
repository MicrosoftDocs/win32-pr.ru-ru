---
description: Задает состояние работоспособности приложения, которое выполняется на виртуальной машине.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'Метод Ивмаппликатионхеалсмонитор:: Сетаппликатионстате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683101"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a><span data-ttu-id="d982e-103">Метод Ивмаппликатионхеалсмонитор:: Сетаппликатионстате</span><span class="sxs-lookup"><span data-stu-id="d982e-103">IVmApplicationHealthMonitor::SetApplicationState method</span></span>

<span data-ttu-id="d982e-104">Задает состояние работоспособности приложения, которое выполняется на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d982e-104">Sets the health state of an application that is running in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d982e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d982e-105">Syntax</span></span>


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a><span data-ttu-id="d982e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d982e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d982e-107">*Идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d982e-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d982e-108">Представление **BSTR** **идентификатора GUID** , идентифицирующее приложение.</span><span class="sxs-lookup"><span data-stu-id="d982e-108">A **BSTR** representation of the **GUID** that identifies the application.</span></span> <span data-ttu-id="d982e-109">Вызывающее приложение отвечает за создание и обслуживание идентификаторов, которые он использует для отслеживаемых приложений.</span><span class="sxs-lookup"><span data-stu-id="d982e-109">It is the calling application's responsibility to create and maintain the identifiers it uses for the applications being monitored.</span></span>

</dd> <dt>

<span data-ttu-id="d982e-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d982e-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d982e-111">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="d982e-111">The display name of the application.</span></span> <span data-ttu-id="d982e-112">Это имя используется в информационной записи журнала событий для изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="d982e-112">This name is used in an informational event log entry for the state change.</span></span>

</dd> <dt>

<span data-ttu-id="d982e-113">*Состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d982e-113">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d982e-114">Значение перечисления [**\_ состояния приложения**](application-state.md) , которое указывает новое состояние работоспособности приложения.</span><span class="sxs-lookup"><span data-stu-id="d982e-114">A value of the [**APPLICATION\_STATE**](application-state.md) enumeration that specifies the new health state of the application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d982e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d982e-115">Return value</span></span>

<span data-ttu-id="d982e-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d982e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d982e-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d982e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d982e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d982e-118">Remarks</span></span>

<span data-ttu-id="d982e-119">Состояние приложений, выполняющихся на виртуальной машине, отражается в  \[ \] значении свойства OperationalStatus 1 класса [**мсвм \_ хеартбеаткомпонент**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="d982e-119">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span>

<span data-ttu-id="d982e-120">Чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d982e-120">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="d982e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d982e-121">Requirements</span></span>



| <span data-ttu-id="d982e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d982e-122">Requirement</span></span> | <span data-ttu-id="d982e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d982e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d982e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d982e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d982e-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d982e-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="d982e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d982e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d982e-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d982e-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d982e-128">Версия</span><span class="sxs-lookup"><span data-stu-id="d982e-128">Version</span></span><br/>                  | <span data-ttu-id="d982e-129">Компоненты интеграции для Windows 8</span><span class="sxs-lookup"><span data-stu-id="d982e-129">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="d982e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d982e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d982e-131"><dt>Вмаппликатионхеалсмонитор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d982e-131"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d982e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d982e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d982e-133">**ивмаппликатионхеалсмонитор**</span><span class="sxs-lookup"><span data-stu-id="d982e-133">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




