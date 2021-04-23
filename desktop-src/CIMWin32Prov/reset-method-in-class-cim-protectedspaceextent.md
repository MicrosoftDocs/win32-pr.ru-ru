---
description: Метод Reset \_ класса CIM протектедспацеекстент запрашивает сброс логического устройства.
ms.assetid: 601e6b0d-4f3c-4a99-aec1-1a769213cf6e
ms.tgt_platform: multiple
title: Метод Reset класса CIM_ProtectedSpaceExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtectedSpaceExtent.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a89d234fc4a134d81485f0e507873fc3cc111305
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142730"
---
# <a name="reset-method-of-the-cim_protectedspaceextent-class"></a><span data-ttu-id="64e38-103">Метод Reset \_ класса CIM протектедспацеекстент</span><span class="sxs-lookup"><span data-stu-id="64e38-103">Reset method of the CIM\_ProtectedSpaceExtent class</span></span>

<span data-ttu-id="64e38-104">Метод **Reset** \_ класса CIM протектедспацеекстент запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="64e38-104">The **Reset** method of the CIM\_ProtectedSpaceExtent class requests a reset of the logical device.</span></span> <span data-ttu-id="64e38-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="64e38-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64e38-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="64e38-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="64e38-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="64e38-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="64e38-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64e38-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="64e38-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64e38-109">Parameters</span></span>

<span data-ttu-id="64e38-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="64e38-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64e38-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64e38-111">Return value</span></span>

<span data-ttu-id="64e38-112">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="64e38-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="64e38-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64e38-113">Remarks</span></span>

<span data-ttu-id="64e38-114">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="64e38-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="64e38-115">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="64e38-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="64e38-116">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="64e38-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="64e38-117">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="64e38-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="64e38-118">Требования</span><span class="sxs-lookup"><span data-stu-id="64e38-118">Requirements</span></span>



| <span data-ttu-id="64e38-119">Требование</span><span class="sxs-lookup"><span data-stu-id="64e38-119">Requirement</span></span> | <span data-ttu-id="64e38-120">Значение</span><span class="sxs-lookup"><span data-stu-id="64e38-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64e38-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64e38-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64e38-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64e38-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64e38-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64e38-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64e38-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64e38-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64e38-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="64e38-125">Namespace</span></span><br/>                | <span data-ttu-id="64e38-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64e38-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64e38-127">MOF</span><span class="sxs-lookup"><span data-stu-id="64e38-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64e38-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64e38-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64e38-129">DLL</span><span class="sxs-lookup"><span data-stu-id="64e38-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64e38-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64e38-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64e38-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64e38-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e38-132">\_ПРОТЕКТЕДСПАЦЕЕКСТЕНТ CIM</span><span class="sxs-lookup"><span data-stu-id="64e38-132">CIM\_ProtectedSpaceExtent</span></span>](reset-method-in-class-cim-protectedspaceextent.md)
</dt> <dt>

[<span data-ttu-id="64e38-133">**\_ПРОТЕКТЕДСПАЦЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="64e38-133">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> </dl>

 

 




