---
description: Метод Invoke \_ класса CIM дискспацечекк оценивает определенную проверку. Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактным \_ подклассом проверки CIM.
ms.assetid: 1f06b0c4-3f39-4a6f-9205-2aa309fb06bb
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_DiskSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbcef752bf412ea255891dd0f5abdf7563f0e078
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655783"
---
# <a name="invoke-method-of-the-cim_diskspacecheck-class"></a><span data-ttu-id="a290f-104">Метод Invoke \_ класса CIM дискспацечекк</span><span class="sxs-lookup"><span data-stu-id="a290f-104">Invoke method of the CIM\_DiskSpaceCheck class</span></span>

<span data-ttu-id="a290f-105">Метод **Invoke** класса [**CIM \_ дискспацечекк**](cim-diskspacecheck.md) оценивает определенную проверку.</span><span class="sxs-lookup"><span data-stu-id="a290f-105">The **Invoke** method of the [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="a290f-106">Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактным подклассом [**\_ проверки CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="a290f-106">The details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclass.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a290f-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a290f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a290f-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a290f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a290f-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a290f-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a290f-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a290f-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a290f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a290f-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="a290f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a290f-112">Parameters</span></span>

<span data-ttu-id="a290f-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a290f-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a290f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a290f-114">Return value</span></span>

<span data-ttu-id="a290f-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="a290f-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a290f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a290f-116">Remarks</span></span>

<span data-ttu-id="a290f-117">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a290f-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a290f-118">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="a290f-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a290f-119">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a290f-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a290f-120">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a290f-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a290f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a290f-121">Requirements</span></span>



| <span data-ttu-id="a290f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a290f-122">Requirement</span></span> | <span data-ttu-id="a290f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a290f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a290f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a290f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a290f-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a290f-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a290f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a290f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a290f-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a290f-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a290f-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a290f-128">Namespace</span></span><br/>                | <span data-ttu-id="a290f-129">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a290f-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a290f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a290f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a290f-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a290f-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a290f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a290f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a290f-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a290f-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a290f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a290f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a290f-135">\_ДИСКСПАЦЕЧЕКК CIM</span><span class="sxs-lookup"><span data-stu-id="a290f-135">CIM\_DiskSpaceCheck</span></span>](invoke-method-in-class-cim-diskspacecheck.md)
</dt> <dt>

[<span data-ttu-id="a290f-136">**\_ДИСКСПАЦЕЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="a290f-136">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> </dl>

 

