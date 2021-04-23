---
description: Метод Invoke \_ класса CIM сеттингчекк оценивает определенную проверку. Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактными \_ подклассами проверки CIM. Этот метод наследуется от \_ проверки CIM.
ms.assetid: b2a9baea-cc5c-43d9-a93c-e3a77823d705
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_SettingCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8c10246e841182aff1b49742694eeb3871d7862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990491"
---
# <a name="invoke-method-of-the-cim_settingcheck-class"></a><span data-ttu-id="547ba-105">Метод Invoke \_ класса CIM сеттингчекк</span><span class="sxs-lookup"><span data-stu-id="547ba-105">Invoke method of the CIM\_SettingCheck class</span></span>

<span data-ttu-id="547ba-106">Метод **Invoke** класса [**CIM \_ сеттингчекк**](cim-settingcheck.md) оценивает определенную проверку.</span><span class="sxs-lookup"><span data-stu-id="547ba-106">The **Invoke** method of the [**CIM\_SettingCheck**](cim-settingcheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="547ba-107">Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактными подклассами [**\_ проверки CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="547ba-107">The details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="547ba-108">Этот метод наследуется **от \_ проверки CIM**.</span><span class="sxs-lookup"><span data-stu-id="547ba-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="547ba-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="547ba-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="547ba-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="547ba-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="547ba-111">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="547ba-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="547ba-112">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="547ba-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="547ba-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="547ba-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="547ba-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="547ba-114">Parameters</span></span>

<span data-ttu-id="547ba-115">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="547ba-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="547ba-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="547ba-116">Return value</span></span>

<span data-ttu-id="547ba-117">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="547ba-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="547ba-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="547ba-118">Remarks</span></span>

<span data-ttu-id="547ba-119">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="547ba-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="547ba-120">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="547ba-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="547ba-121">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="547ba-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="547ba-122">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="547ba-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="547ba-123">Требования</span><span class="sxs-lookup"><span data-stu-id="547ba-123">Requirements</span></span>



| <span data-ttu-id="547ba-124">Требование</span><span class="sxs-lookup"><span data-stu-id="547ba-124">Requirement</span></span> | <span data-ttu-id="547ba-125">Значение</span><span class="sxs-lookup"><span data-stu-id="547ba-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="547ba-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="547ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="547ba-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="547ba-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="547ba-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="547ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="547ba-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="547ba-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="547ba-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="547ba-130">Namespace</span></span><br/>                | <span data-ttu-id="547ba-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="547ba-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="547ba-132">MOF</span><span class="sxs-lookup"><span data-stu-id="547ba-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="547ba-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="547ba-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="547ba-134">DLL</span><span class="sxs-lookup"><span data-stu-id="547ba-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="547ba-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="547ba-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="547ba-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="547ba-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="547ba-137">\_СЕТТИНГЧЕКК CIM</span><span class="sxs-lookup"><span data-stu-id="547ba-137">CIM\_SettingCheck</span></span>](invoke-method-in-class-cim-settingcheck.md)
</dt> <dt>

[<span data-ttu-id="547ba-138">**\_СЕТТИНГЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="547ba-138">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> </dl>

 

