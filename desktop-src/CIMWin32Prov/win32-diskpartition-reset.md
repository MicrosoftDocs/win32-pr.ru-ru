---
description: Запрашивает сброс логического устройства. Этот метод наследуется от CIM-ого модели \_ .
ms.assetid: 2ad40b35-608f-4918-ac66-e3dc53ebe0bb
ms.tgt_platform: multiple
title: Метод Reset класса Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb316a72b801a696b5c5f76376036af75a8beb54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142286"
---
# <a name="reset-method-of-the-win32_diskpartition-class"></a><span data-ttu-id="8ade6-104">Метод Reset \_ класса Win32 дискпартитион</span><span class="sxs-lookup"><span data-stu-id="8ade6-104">Reset method of the Win32\_DiskPartition class</span></span>

<span data-ttu-id="8ade6-105">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8ade6-105">Requests a reset of the logical device.</span></span> <span data-ttu-id="8ade6-106">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="8ade6-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ade6-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8ade6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8ade6-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8ade6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8ade6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ade6-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="8ade6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ade6-110">Parameters</span></span>

<span data-ttu-id="8ade6-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8ade6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ade6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ade6-112">Return value</span></span>

<span data-ttu-id="8ade6-113">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="8ade6-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ade6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ade6-114">Remarks</span></span>

<span data-ttu-id="8ade6-115">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="8ade6-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8ade6-116">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="8ade6-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8ade6-117">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8ade6-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8ade6-118">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8ade6-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ade6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8ade6-119">Requirements</span></span>



| <span data-ttu-id="8ade6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8ade6-120">Requirement</span></span> | <span data-ttu-id="8ade6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8ade6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ade6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ade6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8ade6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ade6-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ade6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ade6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8ade6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ade6-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ade6-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ade6-126">Namespace</span></span><br/>                | <span data-ttu-id="8ade6-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8ade6-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8ade6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="8ade6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ade6-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ade6-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ade6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8ade6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ade6-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ade6-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ade6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ade6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ade6-133">**\_ДИСКПАРТИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="8ade6-133">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="8ade6-134">**\_Дискпартитион Win32**</span><span class="sxs-lookup"><span data-stu-id="8ade6-134">**Win32\_DiskPartition**</span></span>](win32-diskpartition.md)
</dt> </dl>

 

 




