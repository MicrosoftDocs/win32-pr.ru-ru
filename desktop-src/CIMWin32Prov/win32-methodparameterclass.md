---
description: '\_Абстрактный Месодпараметеркласс Win32, базовый класс WMI наследует любой класс, определенный как контейнер значений параметров, которые будут переданы в метод.'
ms.assetid: 293fa378-432d-4e97-a8ab-8dc4917d5476
ms.tgt_platform: multiple
title: Класс Win32_MethodParameterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MethodParameterClass
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e791941df681b2e46c4de6f0714b1290baecfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655702"
---
# <a name="win32_methodparameterclass-class"></a><span data-ttu-id="ef3f6-103">\_Класс Win32 месодпараметеркласс</span><span class="sxs-lookup"><span data-stu-id="ef3f6-103">Win32\_MethodParameterClass class</span></span>

<span data-ttu-id="ef3f6-104">Абстрактный **\_ месодпараметеркласс Win32** , базовый [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) наследует любой класс, определенный как контейнер значений параметров, которые будут переданы в метод.</span><span class="sxs-lookup"><span data-stu-id="ef3f6-104">The **Win32\_MethodParameterClass** abstract, base [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) derives any class defined as a container of parameter values that will be passed to a method.</span></span> <span data-ttu-id="ef3f6-105">Не имея собственных свойств, этот класс выступает в качестве узла классификации.</span><span class="sxs-lookup"><span data-stu-id="ef3f6-105">Having no properties of its own, this class serves as a classification node.</span></span> <span data-ttu-id="ef3f6-106">Аналогичным примером является [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ef3f6-106">A similar example is [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span> <span data-ttu-id="ef3f6-107">Наследование от **CIM \_ фисикалелемент** указывает, что класс описывает физическое, а не логическую сущность.</span><span class="sxs-lookup"><span data-stu-id="ef3f6-107">Derivation from **CIM\_PhysicalElement** indicates that the class describes a physical rather than logical entity.</span></span> <span data-ttu-id="ef3f6-108">В случае с **Win32 \_ месодпараметеркласс** классы, производные от него, создаются специально для передачи параметров в метод.</span><span class="sxs-lookup"><span data-stu-id="ef3f6-108">In the case of **Win32\_MethodParameterClass**, classes derived from it are created specifically to pass parameters to a method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef3f6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef3f6-109">Syntax</span></span>

## <a name="members"></a><span data-ttu-id="ef3f6-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ef3f6-110">Members</span></span>

<span data-ttu-id="ef3f6-111">Класс **Win32 \_ месодпараметеркласс** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="ef3f6-111">The **Win32\_MethodParameterClass** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef3f6-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ef3f6-112">Requirements</span></span>



| <span data-ttu-id="ef3f6-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ef3f6-113">Requirement</span></span> | <span data-ttu-id="ef3f6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ef3f6-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3f6-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef3f6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ef3f6-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef3f6-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef3f6-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef3f6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ef3f6-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef3f6-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef3f6-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef3f6-119">Namespace</span></span><br/>                | <span data-ttu-id="ef3f6-120">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ef3f6-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef3f6-121">MOF</span><span class="sxs-lookup"><span data-stu-id="ef3f6-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef3f6-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f6-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef3f6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ef3f6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef3f6-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef3f6-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef3f6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef3f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef3f6-126">Классы управления службами WMI</span><span class="sxs-lookup"><span data-stu-id="ef3f6-126">WMI Service Management Classes</span></span>](/windows/desktop/CIMWin32Prov/wmi-service-management-classes)
</dt> </dl>

 

