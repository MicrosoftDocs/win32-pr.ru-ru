---
description: Запрашивает, что устройство повторно устанавливает конфигурацию, настройку и/или сведения о состоянии из резервного хранилища.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Метод Ресторепропертиес класса CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664341"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="e4502-103">Метод Ресторепропертиес \_ класса CIM</span><span class="sxs-lookup"><span data-stu-id="e4502-103">RestoreProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="e4502-104">Запрашивает, что устройство повторно устанавливает конфигурацию, настройку и/или сведения о состоянии из резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="e4502-104">Requests that the Device re-establish its configuration, setup and/or state information from a backing store.</span></span> <span data-ttu-id="e4502-105">Цель состоит в том, чтобы записать эти сведения в более раннее время (через метод Савепропертиес) и использовать его для возврата устройства к этому предыдущему условию.</span><span class="sxs-lookup"><span data-stu-id="e4502-105">The intent is to capture this information at an earlier time (via the SaveProperties method), and use it to return a Device to this earlier "condition".</span></span> <span data-ttu-id="e4502-106">Этот метод может не поддерживаться всеми устройствами.</span><span class="sxs-lookup"><span data-stu-id="e4502-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="e4502-107">Метод должен возвращать 0 в случае успеха, 1, если запрос не поддерживается, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="e4502-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="e4502-108">В подклассе можно указать набор возможных кодов возврата, используя квалификатор ValueMap в методе.</span><span class="sxs-lookup"><span data-stu-id="e4502-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="e4502-109">Строки, в которые содержимое ValueMap является переведенными, могут также быть указаны в подклассе как квалификатор массива Values.</span><span class="sxs-lookup"><span data-stu-id="e4502-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4502-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4502-110">Syntax</span></span>


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a><span data-ttu-id="e4502-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4502-111">Parameters</span></span>

<span data-ttu-id="e4502-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e4502-112">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4502-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e4502-113">Requirements</span></span>



| <span data-ttu-id="e4502-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e4502-114">Requirement</span></span> | <span data-ttu-id="e4502-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e4502-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4502-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4502-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e4502-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e4502-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e4502-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4502-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e4502-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e4502-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e4502-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e4502-120">Namespace</span></span><br/>                | <span data-ttu-id="e4502-121">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e4502-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e4502-122">MOF</span><span class="sxs-lookup"><span data-stu-id="e4502-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4502-123"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4502-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4502-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e4502-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4502-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4502-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4502-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4502-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4502-127">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="e4502-127">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




