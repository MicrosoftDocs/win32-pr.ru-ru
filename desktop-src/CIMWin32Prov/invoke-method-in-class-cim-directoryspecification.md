---
description: Метод Invoke \_ класса CIM директориспеЦификатион оценивает определенную проверку.
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_DirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48e5cb315f7dba6be187280ee6a16d7c4711752f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655784"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a><span data-ttu-id="b0065-103">Метод Invoke \_ класса CIM директориспеЦификатион</span><span class="sxs-lookup"><span data-stu-id="b0065-103">Invoke method of the CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="b0065-104">Метод **Invoke** класса [**CIM \_ директориспеЦификатион**](cim-directoryspecification.md) оценивает определенную проверку.</span><span class="sxs-lookup"><span data-stu-id="b0065-104">The **Invoke** method of the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class evaluates a particular check.</span></span> <span data-ttu-id="b0065-105">Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактными подклассами [**\_ проверки CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="b0065-105">Details about how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="b0065-106">Этот метод наследуется **от \_ проверки CIM**.</span><span class="sxs-lookup"><span data-stu-id="b0065-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0065-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b0065-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0065-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0065-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0065-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="b0065-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b0065-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b0065-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0065-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0065-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="b0065-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0065-112">Parameters</span></span>

<span data-ttu-id="b0065-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b0065-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0065-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0065-114">Return value</span></span>

<span data-ttu-id="b0065-115">Возвращает 0 в случае успеха, значение 1, если метод не поддерживается, а любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="b0065-115">Returns a 0 if successful, a 1 if the method is not supported, and any other value indicates an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0065-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0065-116">Remarks</span></span>

<span data-ttu-id="b0065-117">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b0065-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b0065-118">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="b0065-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b0065-119">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b0065-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0065-120">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b0065-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0065-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b0065-121">Requirements</span></span>



| <span data-ttu-id="b0065-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b0065-122">Requirement</span></span> | <span data-ttu-id="b0065-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b0065-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0065-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0065-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0065-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0065-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0065-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0065-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0065-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0065-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0065-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0065-128">Namespace</span></span><br/>                | <span data-ttu-id="b0065-129">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b0065-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0065-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b0065-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0065-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0065-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0065-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b0065-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0065-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0065-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0065-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0065-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0065-135">\_ДИРЕКТОРИСПЕЦИФИКАТИОН CIM</span><span class="sxs-lookup"><span data-stu-id="b0065-135">CIM\_DirectorySpecification</span></span>](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[<span data-ttu-id="b0065-136">**\_ДИРЕКТОРИСПЕЦИФИКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="b0065-136">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> </dl>

 

