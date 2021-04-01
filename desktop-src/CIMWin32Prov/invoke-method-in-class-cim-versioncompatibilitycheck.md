---
description: Метод Invoke \_ класса CIM версионкомпатибилитичекк оценивает определенную проверку.
ms.assetid: d1ccc248-340e-4277-9696-063e1e2bf915
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_VersionCompatibilityCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bccbb6072ae84a238b60247daf6b81cfaa74e608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895697"
---
# <a name="invoke-method-of-the-cim_versioncompatibilitycheck-class"></a><span data-ttu-id="f5394-103">Метод Invoke \_ класса CIM версионкомпатибилитичекк</span><span class="sxs-lookup"><span data-stu-id="f5394-103">Invoke method of the CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="f5394-104">Метод **Invoke** класса [**CIM \_ версионкомпатибилитичекк**](cim-versioncompatibilitycheck.md) оценивает определенную проверку.</span><span class="sxs-lookup"><span data-stu-id="f5394-104">The **Invoke** method of the [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="f5394-105">Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактными подклассами [**\_ проверки CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="f5394-105">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="f5394-106">Этот метод наследуется **от \_ проверки CIM**.</span><span class="sxs-lookup"><span data-stu-id="f5394-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5394-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f5394-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5394-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5394-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5394-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f5394-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f5394-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f5394-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5394-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5394-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f5394-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5394-112">Parameters</span></span>

<span data-ttu-id="f5394-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f5394-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5394-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5394-114">Return value</span></span>

<span data-ttu-id="f5394-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="f5394-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5394-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5394-116">Remarks</span></span>

<span data-ttu-id="f5394-117">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="f5394-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f5394-118">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="f5394-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f5394-119">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f5394-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f5394-120">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f5394-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5394-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f5394-121">Requirements</span></span>



| <span data-ttu-id="f5394-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f5394-122">Requirement</span></span> | <span data-ttu-id="f5394-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f5394-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5394-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5394-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f5394-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5394-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5394-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5394-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f5394-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5394-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5394-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5394-128">Namespace</span></span><br/>                | <span data-ttu-id="f5394-129">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f5394-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5394-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f5394-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5394-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5394-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5394-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f5394-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5394-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5394-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5394-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5394-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5394-135">\_ВЕРСИОНКОМПАТИБИЛИТИЧЕКК CIM</span><span class="sxs-lookup"><span data-stu-id="f5394-135">CIM\_VersionCompatibilityCheck</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md)
</dt> <dt>

[<span data-ttu-id="f5394-136">**\_ВЕРСИОНКОМПАТИБИЛИТИЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="f5394-136">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> </dl>

 

